# Welcome to AndrewDavidoffDocset0426213909

This is a test of tools that convert documents from GenDox HxPrep output to format consumable by docs.microsoft.com. It uses the HTML created by the GenDox build as inline HTML in markdown files.

This is acomplished by building document's docset file structure compatible with Microsoft OPS GitHub publishing, and replacing the .htm extension with .md extension.

## Current limitations
* Document layout is not finalized (work in progress)
* Table formatting (expected to be fixed with custom CSS)
* Generated links go to .htm instead of .html (expected to be fixed with implementation of HTML parsing code)
* Extra HTML tags at the bottom of all pages (expected to be fixed with implementation of HTML parsing code)
* Code boxes don't wrap (expected to be fixed with custom CSS)

