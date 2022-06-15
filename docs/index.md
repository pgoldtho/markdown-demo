## Welcome to GitHub Pages


[markdown tutorial](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

## NAME
**cat** – *concatenate and print files*

## SYNOPSIS
```
cat [-belnstuv] [file ...]

```

## DESCRIPTION

The cat utility reads files sequentially, writing them to the standard output.  The file operands are processed in command-line order.  If file is a single
dash (‘-’) or absent, cat reads from the standard input.  If file is a UNIX domain socket, cat connects to it and then reads it until EOF.  This complements
the UNIX domain binding capability available in inetd(8).

The options are as follows:

Option | Behavior
-- | --
-b |     Number the non-blank output lines, starting at 1.
-e  |    Display non-printing characters (see the -v option), and display a dollar sign (‘$’) at the end of each line.
-l   |   Set an exclusive advisory lock on the standard output file descriptor.  This lock is set using fcntl(2) with the F_SETLKW command.  If the output file is already locked, cat will block until the lock is acquired.
-n  |    Number the output lines, starting at 1.
-s  |    Squeeze multiple adjacent empty lines, causing the output to be single spaced.
-t  |    Display non-printing characters (see the -v option), and display tab characters as ‘^I’.
-u  |    Disable output buffering.
-v  |    Display non-printing characters so they are visible.  Control characters print as ‘^X’ for control-X; the delete character (octal 0177) prints as
‘^?’. |  Non-ASCII characters (with the high bit set) are printed as ‘M-’ (for meta) followed by the character for the low 7 bits.

## EXIT STATUS
The cat utility exits 0 on success, and >0 if an error occurs.

## EXAMPLES
The command:

1. `cat file1` will print the contents of file1 to the standard output.
2. `cat file1 file2 > file3` will sequentially print the contents of file1 and file2 to the file file3, truncating file3 if it already exists.  See the manual page for your shell (e.g., sh(1)) for more information on redirection.
3. `cat file1 - file2 - file3`
    - will print the contents of file1, print data it receives from the standard input until it receives an EOF (‘^D’) character, print the contents of file2,read and output contents of the standard input again, then finally output the contents of file3.
    - Note that if the standard input referred to a file, thesecond dash on the command-line would have no effect, since the entire contents of the file would have already been read and printed by cat when it encountered the first ‘-’ operand.


You can use the [editor on GitHub](https://github.com/pgoldtho/markdown-demo/edit/main/docs/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/pgoldtho/markdown-demo/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
