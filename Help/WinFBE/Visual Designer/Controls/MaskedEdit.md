# MaskedEdit (wfxMaskedEdit)

### Properties

| Name                            | Description                    |
| ------------------------------- | ------------------------------ |
| AllowDrop | Gets or sets a value (true/false) indicating whether the control will accept data that is dragged onto it.|
| BackColor | Gets or sets the background color of the form. Refer to the **Colors** object. |
| BorderStyle | Gets or sets the border style of the control. Refer to the [ControlBorderStyle](#ControlBorderStyle) enum.|
| CtrlId | Gets or sets a value indicating the control ID of the control.|
| CtrlType | Gets or sets the control type value. Always **ControlType.MaskedEdit** and used when adding control to the application’s form collection. |
| DefaultCharacter | Gets or sets the default character that the control substitues for each invalid character in the user input. |
| Enabled | Gets or sets a value (true/false) indicating whether the control can respond to user interaction.|
| Focused | Gets or sets a value (true/false) indicating whether the control has input focus.|
| Font | Gets or sets the font for the control. Refer to the Font object.|
| ForeColor | Gets or sets the foreground color of the control. Refer to the **Colors** object. |
| Height | Gets or sets the height of the control.|
| HideSelection | Gets or sets a value (true/false) indicating whether the selection should be hidden when the control loses focus.|
| hWindow |  Gets the Windows handle (hwnd) of the control. |
| hWindowParent | Gets or sets the Windows handle (hwnd) of the parent control. |
| InputString | Gets or sets a mask template string that specifies the literal characters that can appear at each position in the user input. Use the underscore character as a character placeholder.<br /><br />eg. `(___) ___-____` |
| Left | Gets or sets the distance, in pixels, between the left edge of the control and the left edge of its container's client area (normally the form).|
| Location |Gets or sets the top and left position of the control. Get: returns [wfxPoint](#wfxPoint) object. Set: (left, top). |
| Locked | Gets or sets a value (true/false) indicating whether the control can be moved or resized.|
| MaskString | A mask string that specifies the type of character that can appear at each position in the user input.<br /><br />D:  digit only<br /><br />d: digit only (also allows white space)<br /><br />+: allows + or - or space<br /><br />C: alpha character only<br /><br />c: alpha character or space only<br /><br />A: alpha character only<br /><br />a: alpha character or space only<br /><br /><br/>*: any printable character<br /><br />eg. ` ddd  ddd dddd` |
| Parent | Gets or sets the parent container of the control.|
| ReadOnly | Gets or sets a value (true/false) indicating whether the text can be edited.|
| SelectionStart | Gets or sets a value indicating the start of the selected text.|
| SelectionLength | Gets or sets a value indicating the length of the selected text.|
| Size | Gets or sets the size of the form. Get: returns [wfxSize](#wfxSize) object. Set: (width, height)|
| TabIndex | Gets or sets the position that the control occupies in the TAB position.|
| TabStop | Gets or sets a value (true/false) indicating whether the user can use the TAB key to give focus to the control.|
| Tag | Gets or sets user defined text associated with the form.|
| Text | Gets or sets the text (caption) associated with this form.|
| TextAlign | Gets or sets a value indicating the alignment of the text on a control. Refer to [TextAlignment](#TextAlignment) enum. |
| TextScrollBars | Gets or sets the value to indicate what scrollbars to display. Refer to the [ScrollBars](#ScrollBars) enum.|
| Top | Gets or sets the distance, in pixels, between the top edge of the control and the top edge of its container's client area (normally the form).|
| UseMnemonic | Gets or sets a value (true/false) indicating whether the first character preceded by an ampersand (&) character will be used as the control’s accelerator key.|
| ValidCharacters | Specifies a string of valid characters that the user can enter. Empty string means all characters are valid. For example, if your MaskString allows for "d" digits but you only want the digits 1, 2, 3 to be entered then you would specify ValidCharacters to be 123 |
| Visible | Gets or sets a value (true/false) indicating whether the control is displayed.|
| Width | Gets or sets the width of the control.|

### Methods
| Name                            | Description                    |
| ------------------------------- | ------------------------------ |
| Hide | Conceals the control from the user.|
| Refresh | Forces the form to invalidate its client area and immediately redraw itself and any child controls.|
| SelectNextControl | Moves the input control to the next (True) or previous (False) control in the tab order. |
| SetBounds | Sets the bounds of the control to the specified location and size. SetBounds(left, top, width, height).|
| Show | Creates and displays the control to the user.|

### Events
| Name                            | Description                    |
| ------------------------------- | ------------------------------ |
| AllEvents | Special handler where all events are routed through. Use this handler if you prefer to use the Win32 api style messages and wParam and lParam parameters. Set the Handled element of EventArgs to true if you handle a message and do not want Windows to perform any further processing on the message.|
| Click | Occurs when the client area of the control is clicked.|
| Destroy | Occurs immediately before the control is about to be destroyed and all resources associated with it released.|
| DropFiles | Occurs when an object is dragged and dropped onto the control and the AllowDrop property of the control is set to True.|
| GotFocus | Occurs when the control receives focus.|
| LostFocus | Occurs when the control loses focus.|
| KeyDown | Occurs when a key is pressed while the control has focus.|
| KeyPress | Occurs when a character, space or backspace key is pressed while the control has focus.|
| KeyUp | Occurs when a key is released while the control has focus.|
| MouseDoubleClick | Occurs when the control is double clicked by the mouse.|
| MouseDown | Occurs when the mouse pointer is over the control and a mouse button is pressed.|
| MouseEnter | Occurs when the mouse pointer enters the control.|
| MouseHover | Occurs when the mouse pointer rests on the control.|
| MouseLeave | Occurs when the mouse pointer leaves the control.|
|MouseMove | Occurs when the mouse pointer is moved over the control.|
| MouseUp | Occurs when the mouse pointer is over the control and a mouse button is released.|
| TextChanged | Occurs when the Text property is changed by either a programmatic modification or user interaction.|

##### ControlBorderStyle
```
Enum ControlBorderStyle
   None	= 1
   FixedSingle	
   Fixed3D 
End Enum
```
##### TextAlignment
```
Enum TextAlignment
   Left = 1 
   Right  
   Center 
end enum
```
##### wfxSize
```
Type wfxSize
   private:
      _Width  as Long
      _Height as long 

   public:
      Declare Property Width() As Long
      Declare Property Width( ByVal nValue As Long )
      Declare Property Height() As Long
      Declare Property Height( ByVal nValue As Long )
      Declare Function IsEmpty() as Boolean
      Declare Constructor ( byval nWidth as long = 0, byval nHeight as long = 0)
End Type
```
##### wfxPoint
```
Type wfxPoint
   private:
      _x as Long
      _y as long 

   public:
      Declare Property x() As Long
      Declare Property x( ByVal nValue As Long )
      Declare Property y() As Long
      Declare Property y( ByVal nValue As Long )
      Declare Function IsEmpty() as Boolean
      Declare Constructor ( byval xPos as long = 0, byval yPos as long = 0)
End Type
```
