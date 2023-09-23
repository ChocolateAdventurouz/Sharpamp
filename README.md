Sharpamp - Create Winamp/WACUP plugins in C#
===============================================
Original written by Daniel15 - http://dan.cx/ - revived/upgraded by ChocolateAdventurouz

Download from the [GitHub Releases Page](https://github.com/ChocolateAdventurouz/Sharpamp/tags)

Sharpamp allows you to easily write Winamp/WACUP plugins in C#. It provides a library for access to the
Winamp API, and a Visual Studio template for creating Winamp/WACUP plugins. It **requires** you to have 
Visual Studio 2005, 2008 or 2010. Take a look at the
[Wiki](https://github.com/Daniel15/Sharpamp/wiki) page to see how 
simple it is to get started :)

It supports some basic functionality of the Winamp API, with more coming in the future:  
![Intellisense Menu](http://stuff.dan.cx/images/projects/sharpamp/intellisense.png)

Handling song changes uses standard C# events, and is as simple as:

	public override void Initialize()
	{
		Winamp.SongChanged += Winamp_SongChanged;
	}

	void Winamp_SongChanged(object sender, Daniel15.Sharpamp.SongChangedEventArgs e)
	{
		MessageBox.Show("The song changed to " + e.Song.Title);
	}

A demonstration of what you can do with Sharpamp is shown in the [HelloWorldGUI](https://github.com/Daniel15/Sharpamp/wiki/HelloWorldGUI) sample (included in the download)

Requirements:
=============
 - Visual Studio 2019+ (at least where it is tested)
   - C# and C++ both have to be installed
 - Winamp/WACUP

License
=======
Sharpamp is free software: you can redistribute it and/or modify
it under the terms of the GNU Lesser General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

Sharpamp is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public License
along with Sharpamp.  If not, see <http://www.gnu.org/licenses/>.
