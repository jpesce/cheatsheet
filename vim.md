# Vim

## Netrw - File explorer
Open Netrw on current buffer        :Ex
Open Netrw on in a vertical split   :Vex
Enter directory on tree             gn
New file here                       %
New directory here                  d
Rename file                         R
Delete file                         D

## Fugitive
### View git state on a fullscreen buffer
:0G

Stage file(s)                       s
Unstage file(s)                     u
Togge stage for file(s)             -
Commit                              cc
View inline diff                    =
View vertical split diff            dv

### View current file's previous versions
:0Gclog
Choose a version from quickfix ([q ]q from unimpaired) then view diff to current:
:Gdiff

### Resolving conflict
With the file open, open the three-way vertical split
<leader>gd or :Gvdiffsplit!

Go to next and previous conflict
[c and ]c

Get diff from left pane
<leader>gdh or :diffget //2

Get diff from right pane
<leader>gdl or :diffget //3

## Run/execute external command on current buffer and replace it with the results
%!{program}
Example:
%!jq

## Generate plugins help tags
:helptags ALL

## Colorscheme
### Show a test of a number of highlight groups
:highlight

## Show definitions
### Show command definition
:verbose :com <Command>
Example:
:verbose :com Rg

### Show mapping definition
:verbose :map <Mapping>
Example:
:verbose :map <Space>f

### Show last defined location of option
:verbose set <Option>?
Example:
:verbose set iskeyword?
