# Sublime Text 3 Personal Install Guide

## Download Sublime Text at - https://www.sublimetext.com/3

## Pre-Setup
	Click View - select sidebar - Show Sidebar

## Install Package Control - https://packagecontrol.io/installation
	# Show the consol
		Press: Ctrl + `
	# Paste this code into the consol for ST3:
		import urllib.request,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)

	# Check to see if Package Control installed
		Restart Sublime Text 3
	# Open Package Control
		Press: Ctrl + Shift + P
		type: "install" without quotes in the popup and you should see "Package Control: Install Package" if not Package Control is not installed.


## Theme
	Flatland - https://packagecontrol.io/packages/Theme%20-%20Flatland
		Press: Ctrl + Shift + P
		Type: install
		Type: flatland
		Restart ST3
		Go to: Preferences > Settings
		Paste/Add inside the user Setting file:
			{
			  "theme": "Flatland Dark.sublime-theme",
			  "color_scheme": "Packages/Theme - Flatland/Flatland Dark.tmTheme"
			}

		Save and restart ST3

## Packages - https://packagecontrol.io/
	Emmet - https://packagecontrol.io/packages/Emmet                                 # auto-completion
	AutoFileName - https://packagecontrol.io/packages/AutoFileName                   # Autocomplete Filenames in Sublime Text
	All Autocomplete - https://packagecontrol.io/packages/All%20Autocomplete         # Extends the default autocomplete to find matches in all open files
	Better Completion - https://packagecontrol.io/packages/Better%20Completion       # More auto-completion
	SublimeCodeIntel - https://packagecontrol.io/packages/SublimeCodeIntel           # smart autocomplete

	BracketHighlighter - https://packagecontrol.io/packages/BracketHighlighter       # Bracket Highlighter
	Colorcoder - https://packagecontrol.io/packages/Colorcoder                       # highlight every variable in its own, consistent color
	ColorPicker - https://packagecontrol.io/packages/ColorPicker                     # Pick a color with (ctrl + shift + c)
	Color Highlighter - https://packagecontrol.io/packages/Color%20Highlighter       # previews color values in color

	Origami - https://packagecontrol.io/packages/Origami                             # Split the window however you like! Create new panes, delete panes, move and clone views from pane to pane	
	
	FileOpTabContextMenu - https://packagecontrol.io/packages/FileOpTabContextMenu 	 # adds a few useful options to tab context menu


## Packages with additional settup
	Alignment - https://web.archive.org/web/20150825034957/http://wbond.net/sublime_packages/alignment 	 # alignment of multi-line selections and multiple selections
		# Select the text to align and press Ctrl + Alt + A to use or right click and select: Align By > Alignment - SELECTED 
	AlignTab - https://packagecontrol.io/packages/AlignTab 	# alignment plugin for tables and more
		# Add the Alignment package to the AlignTab Menu and some other options
		Go to Preferences > Package Settings > AlignTab > Content Menu User
			Paste:
				[
				   {"caption" : "-"},
				    {
				      "id": "aligntab",
				      "caption": "Align By",
				      "children": [
				              {
				              "caption" : "#",
				              "command" : "align_tab",
				              "args"    : {"user_input" : "\\#"}
				              },
				              {
				              "caption": "",
				              },
				              {
				              "caption": "Alignment - SELECTED",
				              "command": "alignment"
				              },
				              {
				              "caption": "AlignTab: Live Preview Mode",
				              "command": "align_tab",
				              "args": {"live_preview" : true}
				              },
				              {
				              "caption": "AlignTab: Table Mode",
				              "command": "align_tab",
				              "args": {"mode" : true}
				              }
				      ]
				  }
				]
			

	SideBarEnhancements - https://packagecontrol.io/packages/SideBarEnhancements
		Go to Preferences > Package Settings > Side Bar > Settings - User
			Paste:
			{
				// to remove the menuitem "Donate 20$" from the sidebar context menu.
				"i_donated_to_sidebar_enhancements_developer": "https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=DD4SL2AHYJGBW",
			}

	File​Browser - https://packagecontrol.io/packages/FileBrowser 	# browse your files in a normal tab
		Press: Ctrl + Shift + P  and run this command: Package Control: Satisfy Dependencies
		Paste/Add this to your key bindings: Preferences > Key Bindings
			[
				{
			  "keys": ["f1"],
			  "command": "dired",
			  "args": {
			    "immediate": true,
			    "single_pane": true,
			    "other_group": "right",
			    "project": true
			  }
			}
			]

		restart ST3
		Press F1 to activate the File Browser
		# You can also activate it: 
			Press: Ctrl + Shift + P  and run: Browse Mode...
			Select a folder
			Place the Desktop Tab on another group tab: View > Layout > Columns: 2
		# Commands / Info can be found here: https://github.com/aziz/SublimeFileBrowser


	# GIT - First install Git on the computer - https://git-for-windows.github.io/
	# Check to see if it is working by going to the command line and type: git
		git config --global user.name "USERNAME"
		git config --global user.email "USERNAME@users.noreply.github.com"
	# Install Git and gutter on ST3
		git - https://packagecontrol.io/packages/Git
			Press: Ctrl + Shift + P  and run: Git: Toggle Annotations 	# This will show you changes from THE MASTER(Git Commit)
		gitgutter - https://packagecontrol.io/packages/GitGutter 	# Shows a better icons in the gutter area indicating whether a line has changes from a selected branch - use: GitGutter Master
			# IF POP & GitGutter is not working
				# GitGutter assumes that the git command is available on the command line. If it's not, add the directory containing git.exe to your PATH
				Press: Win + R  and run: cmd
				type: where git
				#use the path for the settings file
				Preferences > Package Settings > Git Gutter > Settings - User
				Paste(EDITED FROM CMD):
					{
					  "git_binary": "C:\\Program Files\\Git\\cmd\\git.exe"
					}

## Other Optional Packages
	View In Browser - https://packagecontrol.io/packages/View%20In%20Browser
	ResourceViewer - https://packagecontrol.io/packages/PackageResourceViewer 	# viewing and editing package resources


# Snippets - http://docs.sublimetext.info/en/latest/extensibility/snippets.html
	# Add Snippets to any package’s folder: Packages > User Folder or install via Package Manager
	Ruby on Rails snippets 	# Autocomplete
	
