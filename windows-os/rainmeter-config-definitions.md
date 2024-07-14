# Rainmeter Config Definitions

| DesktopWorkArea                                                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Defines the [https://docs.microsoft.com/windows/win32/uxguide/winenv-desktop](https://docs.microsoft.com/windows/win32/uxguide/winenv-desktop) for maximized windows. |

With multiple monitors, use DesktopWorkArea@_N_ (where N is the number of the monitor) to set the work area of a specific monitor. DesktopWorkArea and DesktopWorkArea@0 both represent the primary monitor. Note: Moving the taskbar will reset the workarea to Windows' default, as will changing screen resolution. |

<table><thead><tr><th width="556">DesktopWorkAreaType</th><th>Default: 0</th></tr></thead><tbody><tr><td>If set to 1, DesktopWorkArea will be define margins relative to the edges of the screen.</td><td><br></td></tr><tr><td>Example: With DesktopWorkAreaType=0 and DesktopWorkArea=10,20,600,500,</td><td><br></td></tr><tr><td>maximized windows will use an area of 600x500 pixels, which is located</td><td><br></td></tr><tr><td>10 pixels from the left and 20 pixels from the top of the screen. With DesktopWorkAreaType=1 and DesktopWorkArea=10,20,30,40, the area for maximized windows will be 10 pixels from the left, 20 pixels from the top, 30 pixels from the right, and 40 pixels from the bottom of the screen.</td><td><br></td></tr></tbody></table>

#### What I currently use:

`DesktopWorkAreaType=1 DesktopWorkArea@2=0,43,0,48`
