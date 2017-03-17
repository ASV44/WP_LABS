# WP_LABS

Windows Programming

LAB#1 Vdovicenco Alexandru

In order to get this GUI application to work, I didn’t use something special. Development of this “application” was based on Programming Windows by Charlez Petzold, using standard libraries and Visual Studio as IDE.

Our basic task was present in the middle of the screen the given phrase, and this was achieved by using standard function for drawing text “DrawText()”, with specific parameters for aligning our text in the middle of screen. Also at window resize our text must remain in the same position, and this is why, the code which implements this behavior is placed at case “WM_PAINT” in switch menu which handle events. Case “WM_PAINT” is handled every time when window becomes invalid.

Normal Level Task required 2 buttons and 2 text elements, which have custom and default styles. Defaults styled buttons are declared trivial, but custom buttons should be declared in specific mode. For custom button is declared specific style ‘BS_OWNERDRAW'and in order to get button with custom background color we need to use function “FillRect()”, which uses a custom made brush for painting background of button. In order to get custom text elements it is necessary only to create a custom font, using function “CreateFont()” which in some way is trivial.

Advanced Level Task is based on handle events of specific elements, like added buttons and also window button. In order to handle the events of added buttons is used “WM_COMMAND” case of switch, which is handle every time when some button is pressed, adding in inside of current switch, a new switch, we can handle the events from a specific buttons. Our events for handle should be events which interact with other elements of window. This is way at press at some button in this application is changed color of font of one textelement.

During development of this “application”, it is possible to realize what in course of twenty years API’s for development of GUI evolved from a pour and terrible mistake of a nature, to an extreme developer-friendly programing interfaces.  
