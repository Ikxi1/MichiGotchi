## **UI**
- [x] UI opens on right-click
- [ ] toggle to ignore taskbar
	- e.g. in a fullscreen application
- [ ] scale it with windows scaling (or other OS scaling), currently only pixel sizing -> on high DPI/PPI displays it will be very small
## **Click events**
- [x] ``Jared.gd`` needs to check whether a mouse left-click happens on the character or on the UI, otherwise the UI is not clickable
- It can maybe be done with ``mouse_entered()`` & ``mouse_exited`` on the Jared node