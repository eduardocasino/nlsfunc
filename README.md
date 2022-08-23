# nlsfunc
Adds NLS (National Language Support) functionality.

## Syntax
`NLSFUNC [/Y|/?] [[drive:][path]file]`

## Options
<pre>[drive:][path]file
	Drive and path to a valid COUNTRY.SYS file, which contains the country-specific information.`

/Y
Loads the optional yes/no table.

/?
Prints usage.</pre>

## Examples
<pre>	CONFIG.SYS:
		COUNTRY=34,858,C:\FDOS\COUNTRY.SYS

	AUTOEXEC.BAT:
		DISPLAY CON=(EGA,858,2)
		MODE CON CP PREP=((850) C:\FDOS\CPI\EGA.CPI)
		MODE CON CP PREP=((,437) C:\FDOS\CPI\EGA.CPI)
		LH NLSFUNC /Y</pre>

  Then switch code pages using CHCP

If you do not need to change code pages, just omit the MODE lines.

## Copyright
  © 2004 Eduardo Casino, under the terms of the GNU GPL, Version 2

## Notes
  This implementation of NLSFUNC is FreeDOS specific. It won't work with MS-DOS or any other DOS variant.