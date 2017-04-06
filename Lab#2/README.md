# Windows Programming

## LAB#1 Vdovicenco Alexandru

All development process of this laboratory work was based on Programming Windows by
Charlez Petzold book, using Visual Studio IDE with standard libraries.

Basic task of creating a Windows application what will display a dialog box on some event,
was done by creating a resource file "LAB21.rc" where was added a dialog window with input box
and 2 buttons, this dialog windows is initialized and displayed at button press in main window, this
action is handled at message "WM COMMAND". When dialog window is displayed user should
input his name in edit box, and at press "OK" button in dialog window, it will be closed and in
main window, user will see welcome message. Processing of dialog window commands is handled by
function "AboutDlgProc".

System menu is added also by adding in resource filele of menu element, and also by calling
function "LoadMenu", where is indicated the id of menu element. Actions of clicking menu elements
is handled at "WM SYSCOMMANDS" message receiving and where variable "wParam" represent
the id of menu item element.

Hook of keyboard input is performed by adding in resource file of "Accelerator" element where
is indicated id and keyboard shortcut or key associated with this id. Handle of these actions is
performed at the moment of receiving message "WM COMMAND" with "wParam" equal to id from
accelerator list.
For task from Normal Level, is performed change of text color of welcome message from main
window. Color of text can be changed in new dialog window which contains 3 scroll bars which
represent "RGB" values, handle of this process is performed in function "ColorDlgProc()" in which
using id of each scroll bar is handled change of "RGB" value of color.

The Advanced Level task of creation of list box is performed by creating a window with prop-
erties of list box, which is a part of main window, and handling of clicking on list box element s is
performed at receiving "WM COMMAND" with "wParam" equal to id of list box, and by calling
function "SendMessage()" with one parameter being "LB GETCURSEL" we get index of clicked
element from list box.

The cursor is customized by adding new cursor skin in resource file and initiating it by calling
"LoadCursor()" at "WNDCLASS" initialization.