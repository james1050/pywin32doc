# win32pipe

## Module win32pipe

An interface to the win32 pipe API's

#### Methods


  - [GetNamedPipeHandleState](win32pipe.md#win32pipegetnamedpipehandlestate)

    Determines the state of the named pipe.&nbsp;

  - [SetNamedPipeHandleState](win32pipe.md#win32pipesetnamedpipehandlestate)

    Sets the state of the named pipe.&nbsp;

  - [ConnectNamedPipe](win32pipe.md#win32pipeconnectnamedpipe)

    Connects to a named pipe&nbsp;

  - [TransactNamedPipe](win32pipe.md#win32pipetransactnamedpipe)

    Combines the functions that write a 

message to and read a message from the specified named pipe into a single 

network operation.&nbsp;

  - [CallNamedPipe](win32pipe.md#win32pipecallnamedpipe)

    Opens and performs a transaction on a named pipe.&nbsp;

  - [CreatePipe](win32pipe.md#win32pipecreatepipe)

    Creates an anonymous pipe, and returns handles to the read and write ends of the pipe&nbsp;

  - [FdCreatePipe](win32pipe.md#win32pipefdcreatepipe)

    As CreatePipe but returns file descriptors&nbsp;

  - [CreateNamedPipe](win32pipe.md#win32pipecreatenamedpipe)

    Creates an instance of a named pipe and returns a handle for subsequent pipe operations&nbsp;

  - [DisconnectNamedPipe](win32pipe.md#win32pipedisconnectnamedpipe)

    Disconnects the server end of a named pipe instance from a client process.&nbsp;

  - [GetOverlappedResult](win32pipe.md#win32pipegetoverlappedresult)

    Determines the result of the most recent call with an OVERLAPPED object.&nbsp;

  - [WaitNamedPipe](win32pipe.md#win32pipewaitnamedpipe)

    Waits until either a time-out interval elapses or an instance of the specified named pipe is available to be connected to (that is, the pipe's server process has a pending[win32pipe::ConnectNamedPipe](win32pipe.md#win32pipeconnectnamedpipe)operation on the pipe).&nbsp;

  - [GetNamedPipeInfo](win32pipe.md#win32pipegetnamedpipeinfo)

    Returns pipe's flags, buffer sizes, and max instances&nbsp;

  - [PeekNamedPipe](win32pipe.md#win32pipepeeknamedpipe)

    Copies data from a named or anonymous pipe into a buffer without removing it from the pipe. It also returns information about data in the pipe.&nbsp;

  - [GetNamedPipeClientProcessId](win32pipe.md#win32pipegetnamedpipeclientprocessid)

    Returns the process id of client that is connected to a named pipe&nbsp;

  - [GetNamedPipeServerProcessId](win32pipe.md#win32pipegetnamedpipeserverprocessid)

    Returns pid of server process that created a named pipe&nbsp;

  - [GetNamedPipeClientSessionId](win32pipe.md#win32pipegetnamedpipeclientsessionid)

    Returns the session id of client that is connected to a named pipe&nbsp;

  - [GetNamedPipeServerSessionId](win32pipe.md#win32pipegetnamedpipeserversessionid)

    Returns session id of server process that created a named pipe&nbsp;

  - [popen](win32pipe.md#win32pipepopen)

    Version of popen that works in a GUI&nbsp;

#### Comments
Not implemented in py3k.

#### Methods


  - [popen2](win32pipe.md#win32pipepopen2)

    Variation on popen - returns 2 pipes&nbsp;
Not implemented in py3k.

#### Methods


  - [popen3](win32pipe.md#win32pipepopen3)

    Variation on popen - returns 3 pipes&nbsp;
Not implemented in py3k.

#### Methods


  - [popen4](win32pipe.md#win32pipepopen4)

    Like popen2, but stdout/err are combined.&nbsp;
Not implemented in py3k.

## [win32pipe](#win32pipe).CallNamedPipe

string = __CallNamedPipe( *pipeName*  *, data*  *, bufSize*  *, timeOut* __ )
Opens and performs a transaction on a named pipe.

#### Parameters


  -  *pipeName* :[PyUNICODE](#pyunicode)

    The name of the pipe.

  -  *data* : string

    The data to write.

  -  *bufSize* : int

    The size of the result buffer to allocate for the read.

  -  *timeOut* : int

    Specifies the number of milliseconds to wait for the named pipe to be available. In addition to numeric values, the following special values can be specified.


## [win32pipe](#win32pipe).ConnectNamedPipe

int = __ConnectNamedPipe( *hPipe*  *, overlapped* __ )
Connects to a named pipe

#### Parameters


  -  *hPipe* :[PyHANDLE](#pyhandle)

    The handle to the pipe.

  -  *overlapped=None* :[PyOVERLAPPED](#pyoverlapped)

    An overlapped object to use, else None

#### Comments
The result is zero if the function succeeds.  If the function fails, 

GetLastError() is called, and if the result is ERROR_IO_PENDING or ERROR_PIPE_CONNECTED 

(common when passing an overlapped object), this value is returned.  All 

other error values raise a win32 exception (from which the error code 

can be extracted)

## [win32pipe](#win32pipe).CreateNamedPipe

[PyHANDLE](#pyhandle)= __CreateNamedPipe( *pipeName*  *, openMode*  *, pipeMode*  *, nMaxInstances*  *, nOutBufferSize*  *, nInBufferSize*  *, nDefaultTimeOut*  *, sa* __ )
Creates an instance of a named pipe and returns a handle for subsequent pipe operations

#### Parameters


  -  *pipeName* :[PyUnicode](#pyunicode)

    The name of the pipe

  -  *openMode* : int

    OpenMode of the pipe

  -  *pipeMode* : int

    

  -  *nMaxInstances* : int

    

  -  *nOutBufferSize* : int

    

  -  *nInBufferSize* : int

    

  -  *nDefaultTimeOut* : int

    

  -  *sa* :[PySECURITY_ATTRIBUTES](PySECURITY.md#pysecurityattributes)

    

## [win32pipe](#win32pipe).CreatePipe

([PyHANDLE](#pyhandle),[PyHANDLE](#pyhandle)) = __CreatePipe( *sa*  *, nSize* __ )
Creates an anonymous pipe, and returns handles to the read and write ends of the pipe

#### Parameters


  -  *sa* :[PySECURITY_ATTRIBUTES](PySECURITY.md#pysecurityattributes)

    

  -  *nSize* : int

    

## [win32pipe](#win32pipe).DisconnectNamedPipe

 __DisconnectNamedPipe( *hFile* __ )
Disconnects the server end of a named pipe instance from a client process.

#### Parameters


  -  *hFile* :[PyHANDLE](#pyhandle)

    The handle to the pipe to disconnect.

## [win32pipe](#win32pipe).FdCreatePipe

(int, int) = __FdCreatePipe( *sa*  *, nSize*  *, mode* __ )
As CreatePipe but returns file descriptors

#### Parameters


  -  *sa* :[PySECURITY_ATTRIBUTES](PySECURITY.md#pysecurityattributes)

    Specifies security and inheritance for the pipe

  -  *nSize* : int

    Buffer size for pipe.  Use 0 for default size.

  -  *mode* : int

    O_TEXT or O_BINARY

## [win32pipe](#win32pipe).GetNamedPipeClientProcessId

int = __GetNamedPipeClientProcessId( *hPipe* __ )
Returns the process id of client that is connected to a named pipe

#### Parameters


  -  *hPipe* :[PyHANDLE](#pyhandle)

    The handle to the pipe.

#### Comments
Requires Vista or later

## [win32pipe](#win32pipe).GetNamedPipeClientSessionId

int = __GetNamedPipeClientSessionId( *hPipe* __ )
Returns the session id of client that is connected to a named pipe

#### Parameters


  -  *hPipe* :[PyHANDLE](#pyhandle)

    The handle to the pipe.

#### Comments
Requires Vista or later

## [win32pipe](#win32pipe).GetNamedPipeHandleState

(int, int, int/None, int/None,[PyUnicode](#pyunicode)= __GetNamedPipeHandleState( *hPipe*  *, bGetCollectionData* __ )
Determines the state of the named pipe.

#### Parameters


  -  *hPipe* :[PyHANDLE](#pyhandle)

    The handle to the pipe.

  -  *bGetCollectionData=0* : int

    Determines of the collection data should be returned.  If not, None is returned in their place.

## [win32pipe](#win32pipe).GetNamedPipeInfo

(int, int, int, int) = __GetNamedPipeInfo( *hNamedPipe* __ )
Returns pipe's flags, buffer sizes, and max instances

#### Parameters


  -  *hNamedPipe* :[PyHANDLE](#pyhandle)

    Handle to a named pipe

## [win32pipe](#win32pipe).GetNamedPipeServerProcessId

int = __GetNamedPipeServerProcessId( *hPipe* __ )
Returns pid of server process that created a named pipe

#### Parameters


  -  *hPipe* :[PyHANDLE](#pyhandle)

    The handle to the pipe.

#### Comments
Requires Vista or later

## [win32pipe](#win32pipe).GetNamedPipeServerSessionId

int = __GetNamedPipeServerSessionId( *hPipe* __ )
Returns session id of server process that created a named pipe

#### Parameters


  -  *hPipe* :[PyHANDLE](#pyhandle)

    The handle to the pipe.

#### Comments
Requires Vista or later

## [win32pipe](#win32pipe).GetOverlappedResult

int = __GetOverlappedResult( *hFile*  *, overlapped*  *, bWait* __ )
Determines the result of the most recent call with an OVERLAPPED object.

#### Parameters


  -  *hFile* :[PyHANDLE](#pyhandle)

    The handle to the pipe or file

  -  *overlapped* :[PyOVERLAPPED](#pyoverlapped)

    The overlapped object to check.

  -  *bWait* : int

    Indicates if the function should wait for data to become available.

#### Comments
The result is the number of bytes transferred.  The overlapped object's attributes will be changed during this call.

## NMPWAIT_NOWAIT
 __const win32pipe.NMPWAIT_NOWAIT;__ 


## NMPWAIT_USE_DEFAULT_WAIT
 __const win32pipe.NMPWAIT_USE_DEFAULT_WAIT;__ 


## NMPWAIT_WAIT_FOREVER
 __const win32pipe.NMPWAIT_WAIT_FOREVER;__ 


## PIPE_ACCESS_DUPLEX
 __const win32pipe.PIPE_ACCESS_DUPLEX;__ 


## PIPE_ACCESS_INBOUND
 __const win32pipe.PIPE_ACCESS_INBOUND;__ 


## PIPE_ACCESS_OUTBOUND
 __const win32pipe.PIPE_ACCESS_OUTBOUND;__ 


## PIPE_NOWAIT
 __const win32pipe.PIPE_NOWAIT;__ 


## PIPE_READMODE_BYTE
 __const win32pipe.PIPE_READMODE_BYTE;__ 


## PIPE_READMODE_MESSAGE
 __const win32pipe.PIPE_READMODE_MESSAGE;__ 


## PIPE_TYPE_BYTE
 __const win32pipe.PIPE_TYPE_BYTE;__ 


## PIPE_TYPE_MESSAGE
 __const win32pipe.PIPE_TYPE_MESSAGE;__ 


## PIPE_UNLIMITED_INSTANCES
 __const win32pipe.PIPE_UNLIMITED_INSTANCES;__ 


## PIPE_WAIT
 __const win32pipe.PIPE_WAIT;__ 


## [win32pipe](#win32pipe).PeekNamedPipe

(string, int, int) = __PeekNamedPipe( *hPipe*  *, size* __ )
Copies data from a named or anonymous pipe into a buffer without removing it from the pipe. It also returns information about data in the pipe.

#### Parameters


  -  *hPipe* :[PyHANDLE](#pyhandle)

    The handle to the pipe.

  -  *size* : int

    The size of the buffer.

## [win32pipe](#win32pipe).SetNamedPipeHandleState

 __SetNamedPipeHandleState( *hPipe*  *, Mode*  *, MaxCollectionCount*  *, CollectDataTimeout* __ )
Sets the state of the named pipe.

#### Parameters


  -  *hPipe* :[PyHANDLE](#pyhandle)

    The handle to the pipe.

  -  *Mode* : int/None

    The pipe read mode.

  -  *MaxCollectionCount* : int/None

    Maximum bytes collected before transmission to the server.

  -  *CollectDataTimeout* : int/None

    Maximum time to wait, in milliseconds, before transmission to server.

## [win32pipe](#win32pipe).TransactNamedPipe

string/buffer = __TransactNamedPipe( *pipeName*  *, writeData*  *, buffer/bufSize*  *, overlapped* __ )
Combines the functions that write a 

message to and read a message from the specified named pipe into a single 

network operation.

#### Parameters


  -  *pipeName* :[PyUNICODE](#pyunicode)

    The name of the pipe.

  -  *writeData* : string/buffer

    The data to write to the pipe.

  -  *buffer/bufSize* :[PyOVERLAPPEDReadBuffer](#pyoverlappedreadbuffer)/int

    Size of the buffer to create for the result, 

or a buffer to fill with the result. If a buffer object and overlapped is passed, the result is 

the buffer itself.  If a buffer but no overlapped is passed, the result is a new string object, 

built from the buffer, but with a length that reflects the data actually read.

  -  *overlapped=None* :[PyOVERLAPPED](#pyoverlapped)

    An overlapped structure or None

#### Comments
This function is modelled on[win32file::ReadFile](win32file.md#win32filereadfile)- for overlapped 

operations you are expected to provide a buffer which will be filled 

asynchronously.

## [win32pipe](#win32pipe).WaitNamedPipe

 __WaitNamedPipe( *pipeName*  *, timeout* __ )
Waits until either a time-out interval elapses or an instance of the specified named pipe is available to be connected to (that is, the pipe's server process has a pending[win32pipe::ConnectNamedPipe](win32pipe.md#win32pipeconnectnamedpipe)operation on the pipe).

#### Parameters


  -  *pipeName* :[PyUnicode](#pyunicode)

    The name of the pipe

  -  *timeout* : int

    The number of milliseconds the function will wait. 

instead of a literal value, you can specify one of the following values for the timeout:


## [win32pipe](#win32pipe).popen

pipe = __popen( *cmdstring*  *, mode* __ )
Popen that works from a GUI.

#### Parameters


  -  *cmdstring* : string

    The cmdstring to pass to the shell

  -  *mode* : string

    Either 'r' or 'w'

#### Return Value
The result of this function is a pipe (file) connected to the 

processes stdin or stdout, depending on the requested mode.

## [win32pipe](#win32pipe).popen2

(pipe, pipe) = __popen2( *cmdstring*  *, mode* __ )
Variation on[win32pipe::popen](win32pipe.md#win32pipepopen)

#### Parameters


  -  *cmdstring* : string

    The cmdstring to pass to the shell

  -  *mode* : string

    Either 't' or 'b'

#### Return Value
The result of this function is a pipe (file) connected to the 

processes stdin, and a pipe connected to the processes stdout.

## [win32pipe](#win32pipe).popen3

(pipe, pipe, pipe) = __popen3( *cmdstring*  *, mode* __ )
Variation on[win32pipe::popen](win32pipe.md#win32pipepopen)

#### Parameters


  -  *cmdstring* : string

    The cmdstring to pass to the shell

  -  *mode* : string

    Either 't' or 'b'

#### Return Value
The result of this function is 3 pipes - the processes stdin, stdout and stderr

## [win32pipe](#win32pipe).popen4

(pipe, pipe) = __popen4( *cmdstring*  *, mode* __ )
Variation on[win32pipe::popen](win32pipe.md#win32pipepopen)

#### Parameters


  -  *cmdstring* : string

    The cmdstring to pass to the shell

  -  *mode* : string

    Either 't' or 'b'

#### Return Value
The result of this function is 2 pipes - the processes stdin, 

and stdout+stderr combined as a single pipe.