# VS Code LS-DYNA extension
<img alt="Visual Studio Marketplace Version" src="https://img.shields.io/visual-studio-marketplace/v/ryanosullivan.lsdyna?style=for-the-badge">
<img alt="GitHub Workflow Status" src="https://img.shields.io/github/workflow/status/osullivryan/vscode-lsdyna/Release Vscode Plugin?style=for-the-badge">

## Integrates [LS-DYNA](https://www.lstc.com/) into VS Code.

This extension integrates LS-DYNA formatting and keyword snippets into VS Code. 

### Example
![](images/Example.gif)

### Contributing new Keywords

There are a few ways you can go about adding keywords or features:

1. Send me an email or message on Github with the desired keyword (and an example).
2. Make a pull request:  
    1. Create a fork of the master.
    2. Add your new keyword(s) under the `keywords/` directory.
    3. Run the `processing.ipynb` script to process the keywords into VSCode snippet format.
    4. Create a new pull request to merge your branch into this master. 
    5. After the pull request is accepted 

### Some References. 

[vim-lsdyna](https://github.com/gradzikb/vim-lsdyna)  
[DCHartlen's vscode extension](https://github.com/DCHartlen/LSDynaForVSCode)

# dl
## about
- Script "processing.ipynb" processes a set of .k files in subdirectories (excluding those whose top-level directory name starts with an underscore).     
- Each entry in the JSON represents a keyword snippet derived from a .k file, with placeholders like ?title?, ?path?, etc., replaced by $1, $2, etc., for use in snippet expansion.
- This JSON can be dropped into the snippets folder of a VSCode extension or workspace settings, so that when a user types a keyword (like *DATABASE_BINARY_D3PLOT), VSCode will auto-suggest it and allow tabbing through the $1, $2, etc., fields.

## TODO
- card ended start and end with $-line