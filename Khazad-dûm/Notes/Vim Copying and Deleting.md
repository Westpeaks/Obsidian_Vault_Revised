04-07-2025 17:07

Tags: [[Vim]] [[Programming Fundamentals]] [[Linux]]

## Terminology

The keyboard shortcuts to copy, cut, and paste can be boiled down into three characters that utilize Vim-specific terminology.

Understanding these terms will help you recall the correct keyboard shortcut.

- Y stands for “yank” in Vim, which is conceptually similar to copying.
- D stands for “delete” in Vim, which is conceptually similar to cutting.
- P stands for “put” in Vim, which is conceptually similar to pasting.
## Copying in Vim

- **yy:** Copy the current line in vi
- **3yy:** To yank multiple lines in vim, type in the number of lines followed by yy. This command will copy (yank) 3 lines starting from your cursor position.
- **y$:** Copy everything from the cursor to the end of the line
- **y^:** Copy everything from the start of the line to the cursor.
- **yiw:** Copy the current word.

## Deleting in Vim

- **dd:** Cut the current line
- **3dd:** Cut 3 lines, starting from the cursor
- **d$:** Cut everything from the cursor to the end of the line

## Pasting in Vim 

- **P (uppercase):** Paste before your cursor
- **p (lowercase):** Paste after your cursor
## References

[# Copy & Paste in Vim / Vi](https://www.warp.dev/terminus/vim-copy-paste)

