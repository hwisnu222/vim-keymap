#Netrw - file manager vim


open file manager netrw using command

```bash
:Explore     " open file explorer di direktori file saat ini
:Vexplore    " open with split vertikal
:Sexplore    " open with split horizontal
:Texplore    " open with tab baru
:Netrw       " Alias for :Explore
```


**Additional:**
- `Enter` : Open file/direktory
- `-` : move to up parent directory
- `D` : Remove file/direktory (confirmation)
- `R` : Rename file/direktory
- `%` : Create new file
- `d` : create new directory


```vim
:edit .      " Open Netrw in current directory
:Lexplore    " Open explorer in left side (toggle)
:NetrwDel X  " delete file X
:NetrwRename X Y  " rename file X to Y
```



### Resources:
- https://vonheikemen.github.io/devlog/tools/using-netrw-vim-builtin-file-explorer/