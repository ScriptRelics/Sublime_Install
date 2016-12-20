# Sublime Text 3

# Download Sublime Text at - https://www.sublimetext.com/3

# Pre-Setup
	Click View - select sidebar -

# Install Package Control - https://packagecontrol.io/installation
	# Show the consol
		Press: Ctrl + `
	# Paste this code into the consol for ST3:
		import urllib.request,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)

	# Check to see if Package Control installed
		Restart Sublime Text 3
	# Open Package Control
		Press: Ctrl + Shift + P
		type: "install" without quotes in the popup and you should see "Package Control: Install Package" if not Package Control is not installed.


# Theme
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


# Packages 
	Emmet - https://packagecontrol.io/packages/Emmet                            	        # auto-completion
	AutoFileName - https://packagecontrol.io/packages/AutoFileName              	        # Autocomplete Filenames in Sublime Text
	All Autocomplete - https://packagecontrol.io/packages/All%20Autocomplete    	        # Extends the default autocomplete to find matches in all open files
	Better Completion - https://packagecontrol.io/packages/Better%20Completion  	        # More auto-completion

	Bracket​Highlighter - https://packagecontrol.io/packages/BracketHighlighter  	        # Bracket​ Highlighter
	Colorcoder - https://packagecontrol.io/packages/Colorcoder                  	        # highlight every variable in its own, consistent color
	Color​Picker - https://packagecontrol.io/packages/Color​Picker                	        # Pick a color with (ctrl + shift + c)
	Color Highlighter - https://packagecontrol.io/packages/Color%20Highlighter  	        # previews color values in color

	Origami - https://packagecontrol.io/packages/Origami                                    # Split the window however you like! Create new panes, delete panes, move and clone views from pane to pane	
	
	File​Op​Tab​Context​Menu - https://packagecontrol.io/packages/FileOpTabContextMenu 	        # adds a few useful options to tab context menu


# Packages with additional settup
	Alignment - https://web.archive.org/web/20150825034957/http://wbond.net/sublime_packages/alignment 	# alignment of multi-line selections and multiple selections
	Align​Tab - https://packagecontrol.io/packages/AlignTab 	# alignment plugin for tables and more
		Go to Preferences > Package Settings > Align​Tab > Content Menu User
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
			

	Side​Bar​Enhancements - https://packagecontrol.io/packages/SideBarEnhancements
		Go to Preferences > Package Settings > Side Bar > Settings - User
			Paste:
			{
				// to remove the menuitem "Donate 20$" from the sidebar context menu.
				"i_donated_to_sidebar_enhancements_developer": "https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=DD4SL2AHYJGBW",
			}

	git - https://packagecontrol.io/packages/Git
	gitgutter - https://packagecontrol.io/packages/GitGutter 	#show an icon in the gutter area indicating whether a line has been inserted, modified or deleted
			#GitGutter assumes that the git command is available on the command line. If it's not, add the directory containing git.exe to your PATH

# Other Packages
	View In Browser - https://packagecontrol.io/packages/View%20In%20Browser
	ResourceViewer - https://packagecontrol.io/packages/PackageResourceViewer 	# viewing and editing package resources


# Preferances File
	{
		"color_scheme": "Packages/Colorcoder/Flatland Dark (Colorcoded).tmTheme",
		"original_color_scheme": "Packages/Theme - Flatland/Flatland Dark.tmTheme",
		"theme": "Flatland Dark.sublime-theme",
		
		"auto_complete_commit_on_tab": true,
		"spell_check": true,
	}


