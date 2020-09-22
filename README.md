<div align="center">

## BrowseForFolder class


</div>

### Description

More code from me shwoing the .NET way to do common things that used to require mucho API.. This is a BrowseForFolder class that uses the .NET framework only... Havent seen this done yet without API. Enjoy..and please vote if you like it and use it.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Chris Andersen](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/chris-andersen.md)
**Level**          |Beginner
**User Rating**    |5.0 (35 globes from 7 users)
**Compatibility**  |C\#
**Category**       |[Controls/ Forms/ Dialogs/ Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/controls-forms-dialogs-menus__10-3.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/chris-andersen-browseforfolder-class__10-199/archive/master.zip)





### Source Code

```
// created on 04/11/2002 at 6:29 PM
// by Chris Andersen using SharpDevelop http://www.icsharpcode.net
// This class give you the BrowseForfolder dialog without using the API.
// Sample usage
		/* BrowseForFolder test = new BrowseForFolder();
			MessageBox.Show(test.ShowIt("bwah"));
		*/
using System;
using System.Windows.Forms;
using System.Windows.Forms.Design;
public class BrowseForFolder : FolderNameEditor
{
	// inherit the FolderNameEditor class
	FolderNameEditor.FolderBrowser fBrowser;
	public BrowseForFolder()
	{
		// contructor
		// create an instance of FolderBrowser
		fBrowser = new System.Windows.Forms.Design.FolderNameEditor.FolderBrowser();
	}
	public string ShowIt(string textdescription)
	{
		// set the Description label
		fBrowser.Description = textdescription;
		fBrowser.ShowDialog(); // show the Windows
		return fBrowser.DirectoryPath;  // return whatever path choosen
	}
	~BrowseForFolder()
	{
		// destructor
		fBrowser.Dispose();
	}
}
```

