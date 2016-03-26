# PyCEditView

## PyCEditView Object

A class which implementes a CView of a text file.  Derived from[PyCView](#pycview)and[PyCEdit](#pycedit)objects.

#### Methods


  - [IsModified](PyCEditView.md#pyceditviewismodified)

    Indicates if the view's document is modified.&nbsp;

  - [LoadFile](PyCEditView.md#pyceditviewloadfile)

    Loads a named file into the view.&nbsp;

  - [SetModifiedFlag](PyCEditView.md#pyceditviewsetmodifiedflag)

    Sets the view's document modified flag.&nbsp;

  - [GetEditCtrl](PyCEditView.md#pyceditviewgeteditctrl)

    Returns the underlying[PyCEdit](#pycedit)object&nbsp;

  - [PreCreateWindow](PyCEditView.md#pyceditviewprecreatewindow)

    Calls the underlying MFC PreCreateWindow method.&nbsp;

  - [SaveFile](PyCEditView.md#pyceditviewsavefile)

    Saves the view to a named file.&nbsp;

  - [OnCommand](PyCEditView.md#pyceditviewoncommand)

    Calls the standard Python framework OnCommand handler&nbsp;


## [PyCEditView](#pyceditview).GetEditCtrl

 __PyCEditCtrl__ = __GetEditCtrl(__ )
returns the underlying edit control object.

## [PyCEditView](#pyceditview).IsModified

int = __IsModified(__ )
Indicates if the view's document has the modified flag set.

## [PyCEditView](#pyceditview).LoadFile

 __LoadFile( *fileName* __ )
Loads a file into the view.

#### Parameters


  -  *fileName* : string

    The name of the file to be loaded.

## [PyCEditView](#pyceditview).OnCommand

 __OnCommand( *wparam*  *, lparam* __ )
Calls the standard Python framework OnCommand handler

#### Parameters


  -  *wparam* : int

    

  -  *lparam* : int

    

#### See Also


  - [PyCWnd.OnCommand](PyCWnd.md#pycwndoncommand_virtual)virtual method

## [PyCEditView](#pyceditview).PreCreateWindow

tuple = __PreCreateWindow( *createStruct* __ )
Calls the underlying MFC PreCreateWindow method.

#### Parameters


  -  *createStruct* : tuple

    A tuple representing a CREATESTRUCT structure.

## [PyCEditView](#pyceditview).SaveFile

 __SaveFile( *fileName* __ )
Saves the view to a file.

#### Parameters


  -  *fileName* : string

    The name of the file to be written.

## [PyCEditView](#pyceditview).SetModifiedFlag

 __SetModifiedFlag( *bModified* __ )
Sets the modified flag for the view's document.

#### Parameters


  -  *bModified=1* : int

    The modified state to set.