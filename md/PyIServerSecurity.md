# PyIServerSecurity

## PyIServerSecurity Object

Interface used to access client security settings and perform impersonation

#### Comments
Can be created using[pythoncom::CoGetCallContext](pythoncom.md#pythoncomcogetcallcontext)

#### Methods


  - [QueryBlanket](PyIServerSecurity.md#pyiserversecurityqueryblanket)

    Retrieves security settings specified by the client&nbsp;

  - [ImpersonateClient](PyIServerSecurity.md#pyiserversecurityimpersonateclient)

    Initiates impersonation of client&nbsp;

  - [RevertToSelf](PyIServerSecurity.md#pyiserversecurityreverttoself)

    Ends impersonation of client&nbsp;

  - [IsImpersonating](PyIServerSecurity.md#pyiserversecurityisimpersonating)

    Determines if server is currently impersonating a client&nbsp;

## [PyIServerSecurity](#pyiserversecurity).ImpersonateClient

 __ImpersonateClient(__ )
Initiates impersonation of client

## [PyIServerSecurity](#pyiserversecurity).IsImpersonating

bool = __IsImpersonating(__ )
Determines if server is currently impersonating a client

## [PyIServerSecurity](#pyiserversecurity).QueryBlanket

dict = __QueryBlanket( *Capabilities* __ )
Retrieves security settings specified by the client

#### Parameters


  -  *Capabilities=0* : int

    Can be EOAC_MAKE_FULLSIC for SChannel provider

## [PyIServerSecurity](#pyiserversecurity).RevertToSelf

 __RevertToSelf(__ )
Ends impersonation of client