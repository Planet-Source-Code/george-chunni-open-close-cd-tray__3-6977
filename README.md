<div align="center">

## Open / Close CD Tray


</div>

### Description

This code just shows you how to open and close the cd tray, pretty straight forward
 
### More Info
 
You need to link the lib file, winmm.lib, if you are using Dev-C++ the file is libwinmm.a


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[George Chunni](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/george-chunni.md)
**Level**          |Intermediate
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |C, C\+\+ \(general\)
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__3-1.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/george-chunni-open-close-cd-tray__3-6977/archive/master.zip)





### Source Code

```
// Look into the mciSendString function, it can do a lot of interesting things, Have Fun
#include <windows.h>
#include <mmsystem.h>
int main(int argc, char *argv[])
{
HWND hwnd = FindWindow(0, argv[0]); // Find our program window
ShowWindow(hwnd, SW_HIDE); // Hides it
for(;;)
{
mciSendString("Set CDAudio Door Open wait", 0, 0, 0); // Opens Cd Tray
mciSendString("Set CDAudio Door Closed wait", 0, 0, 0); // Closes CD tray
}
}
```

