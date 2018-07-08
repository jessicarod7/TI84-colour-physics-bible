# Contributing Guidelines

If you want to contribute to The Physics Bible, please follow the instructions below to ensure the stability and reliability of the project.

## Reporting Issues

**Include the following elements in your report (required):**

- What was happening before the issue appeared
- Steps to reproduce the issue
- The expected output
- What actually happened (include any error messages that appear)

If you are able to, include the code where the error occurred by following the steps below:

1. **Ensure the program is in RAM.** Press ```2nd``` and then ```0``` (```catalog```). Scroll to ```UnArchive```, and hit ```enter```. Next, go to ```pgrm```, scroll to ```PHYSBBLE```, and press ```enter``` again. Finally, press enter to move the program to RAM. If an error appears, you do not have enough RAM, so stop here and continue with filing the issue report.
2. Execute the program again until you get to the error. Then tap ```2``` and the calculator will scroll to the error. This may take a while, so be patient and dont hit any buttons.
3. When you reach the error, retype the preceding and following lines of code into the end of your issue report. Turn it into block code by double spacing from other text and using \``` one lines above and below the code.
4. Repeat Step 1 to return your program to RAM, except scroll to ```Archive``` instead.

## Contributing To The Program

### Required Tools

- A GitHub account
- [The TI Connect CE program](https://education.ti.com/en/products/computer-software/ti-connect-ce-sw)
- A TI-84+CE or TI-84+C SE (as applicable), or an emulator and the respective ```.rom``` file

### Preparing to Edit

To edit this project, you will need to fork it to your own GitHub account. When making changes, it's recommended to create a new branch, so that a stable release copy is available for comparison.

### Editing Practices

- **Make all changes in the ```.txt``` file, rather then directly editing the ```.8xp``` file.** This makes it much easier for everyone to review the changes made then comparing line by line in *TI Connect CE* or on a calculator.
- **Format according to the TI Connect CE style.** All ```.txt``` source files in this program are designed for full compatibility with the *TI Connect CE* program editor; in other words, the text files should be able to be directly copied into *TI Connect CE* and compile correctly. There are a few steps to ensure this compatibility:
  - Do not include any line-leading colons in your ```.txt``` file, *TI Connect CE* will add these automatically.
  - Use the specific symbols from *TI Connect CE*, not your own or from other compilers. This includes symbols such as ```­``` (the negative sign), which may not display on all devices or text editors. The easiest way to ensure this is by copying the symbols from *TI Connect CE* by double clicking the symbol in the program editor (which will input it into a blank program file), and then copying them over.
  - Watch your spacing with commands. If a command requires a space (or lack of one) after it, the command will fail upon execution, even if nothing follows the command on that line. Again, check *TI Connect CE* for proper formatting.
- **Comment your work.** Excessive commenting is not helpful, but commenting on new features helps you and others to find issues if something goes wrong. Use the following template for your comments:

```
While 0
"=COMMENT TEXT GOES HERE="
End
```

- **Update the ```.8xp```program file with each commit.** This is the file that will be posted in the final release, and will be used if others download the source code, so it is important that the program is ready to run. ***The program variable name is always ```PHYSBBLE```.***

### Preparation for a Pull Request

- **Make sure the ```.8xp``` file is updated.** Barring any inconsistencies, this will be the file provided in the release.
- **Restore the ```.gitignore``` file to as it is in the** ***master*** **branch.** This generally should not change between releases.
- **Rebase your work onto the source** ***master*** **branch, and clear any conflicts**. The best way to sync to the main branch is by adding this remote repository to pull from. [Click here for an explanation.](https://medium.com/@ruthmpardee/git-fork-workflow-using-rebase-587a144be470)

### Making the Pull Request

- **Use a good title.** The title should quickly convey what improvements your work introduces.
- **Provide a brief but through explanation of your changes.** The description should give a short summary of what changes have been made, and what commands were changed to do so.
- **Include images (if applicable).** This makes it easier to see how the program works with your changes. Usually this is only needed for user-facing changes.
