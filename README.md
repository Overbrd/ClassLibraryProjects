# ClassLibraryProjects

Class Libraries

1.	Create a Solution
2.	Create a Class Library Project
3.	Add a Console App To The Solution
4.	Add a Project Reference
5.	Set Console App as Start Up Project
6.	Run The App

SOLUTION: 
ClassLibraryProjects

PROJECTS:
ShowCase -	(Program.cs)

StringLibrary -	(Class1.cs)

A class library defines types and methods that are called by an application. 

When you create a class library, you can distribute it as a NuGet package or as a component bundled with the application that uses it.

Class1.cs:

namespace UtilityLibraries
{
    public static class StringLibrary
    {
        public static bool StartsWithUpper(this string str)
        {
            if (string.IsNullOrWhiteSpace(str))
                return false;

            char ch = str[0];
            return char.IsUpper(ch);
        }
    }
} 

The class library, UtilityLibraries.StringLibrary, contains a method named StartsWithUpper. This method returns a Boolean value that indicates whether the current string instance begins with an uppercase character. The Unicode standard distinguishes uppercase characters from lowercase characters. The Char.IsUpper(Char) method returns true if a character is uppercase.
StartsWithUpper is implemented as an extension method so that you can call it as if it were a member of the String class.

Program.cs:

using UtilityLibraries;

This code (placed at the top of Program.cs) allows you to incorporate the Class1.cs class library on the apps Program.cs page.
You must also, in Solution Explorer, right-click the ShowCase project's Dependencies node, and select Add Project Reference

Add Unit Tests

1.	Create a unit test project
2.	Add a project reference
3.	Add and run unit test methods
4.	Handle test failures
5.	Test the Release version of the library
6.	Debug tests
