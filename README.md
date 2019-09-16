# SendInputKeyCommands
Custom wrapper for user23 SendInput keyboard commands
________________________________________________________________

- Reference SendInputKeyCommands.dll in your script.
- Create new instance of SendInputKeyCommands
- Call a SendKey method = win.
________________________________________________________________

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
	

