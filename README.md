# SendInputKeyCommands
Custom wrapper for user23 SendInput keyboard commands
________________________________________________________________

- Reference SendInputKeyCommands.dll in your script.
- Create new instance of SendInputKeyCommands
- Call a SendKey method = win.
________________________________________________________________

This wrapper with convert strings to VirtualKeyCodes for use with SendInput.
It will also detect and use Shift to enter symbols or uppercase letters.
The option for using VirtualKeyCodes directly is still there.

Setup Example:

	using System;
	using SendInputKeyCommands;

	namespace YourHotkeyProgram
	{
	    public static YourClass()
	    {
		public static void Test()
		{
		  SendInputKeyCommand sendKeyComm = new SendInputKeyCommand();

		  //Example1:
		  string sentence = "This is a sentence.";
		  foreach (char c in sentence)
		  { sendKeyComm.SendKeyPress(c.ToString()); }

		  //Example2:
		  sendKeyComm.SendKeyDown("CTRL");
		  sendKeyComm.SendKeyPress("v");
		  sendKeyComm.SendKeyUp("CTRL");

		  //Example3:
		  sendKeyComm.SendKeyPress(SendInputKeyCommand.VirtualKeyCode.HOME);

		  //Example3b:
		  sendKeyComm.SendKeyPress("Home");
		}
	    }
	}
	

