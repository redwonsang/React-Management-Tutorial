" .ideavimrc is a configuration file for IdeaVim plugin. It uses
"   the same commands as the original .vimrc configuration.
" You can find a list of commands here: https://jb.gg/h38q75
" Find more examples here: https://jb.gg/share-ideavimrc


"" -- Suggested options --
" Show a few lines of context around the cursor. Noten-prefix) that this makes the
" text scroll if you mouse-click near the start or end of the window.
let mapleader=" "
set scrolloff=3

" Do incremental searching.
set incsearch
set clipboard=unnamed

" Don't use Ex mode, use Q for formatting.
map Q gq

" --- Enable IdeaVim plugins https://jb.gg/ideavim-plugins

" Highlight copied text
Plug 'machakann/vim-highlightedyank'
" Commentary plugin
Plug 'tpope/vim-commentary'
Plug 'easymotion/vim-easymotion'
Plug 'vim-scripts/argtextobj.vim'
"Plug 'vim-multiple-cursors'

imap jj <Esc>
set surround
set NERDTree
set peekaboo
set argtextobj
set exchange
"set which-key
set commentary
set ReplaceWithRegister
set switch
set multiple-cursors
let g:WhichKey_FontSize = 17

"true

" --------------------
" open ideavimrc file
" source ideavimrc file
" --------------------
map <leader>vs :source ~/.ideavimrc<CR>
map <leader>vi :e ~/.ideavimrc<CR>
map <leader>t :NERDTree<cr>
map <leader>f <Action>(SelectInProjectView)

" Remap multiple-cursors shortcuts to match terryma/vim-multiple-cursors
nmap <C-n> <Plug>NextWholeOccurrence
xmap <C-n> <Plug>NextWholeOccurrence
nmap g<C-n> <Plug>NextOccurrence
xmap g<C-n> <Plug>NextOccurrence
xmap <C-x> <Plug>SkipOccurrence
xmap <C-p> <Plug>RemoveOccurrence

" Note that the default <A-n> and g<A-n> shortcuts don't work on Mac due to dead keys.
" <A-n> is used to enter accented text e.g. ñ
" Feel free to pick your own mappings that are not affected. I like to use <leader>
nmap <leader><C-n> <Plug>AllWholeOccurrences
xmap <leader><C-n> <Plug>AllWholeOccurrences
nmap <leader>g<C-n> <Plug>AllOccurrences
xmap <leader>g<C-n> <Plug>AllOccurrences

" Orsymotion-prefix) use - and +
nnoremap - :Switch<CR>
nnoremap + :SwitchReverse<CR>
" Enable all patterns from multiple groups
let g:switch_definitions = 'group:basic,group:java,group:rspec'
" Enable specific patterns
let g:switch_definitions = 'basic_true_false,java_visibility,rspec_should'
" Mix groups and individual patterns
let g:switch_definitions = 'group:basic,java_visibility,rspec_should'
"" -- Map IDE actions to IdeaVim -- https://jb.gg/abva4t
"" Map \r to the Reformat Code action
"map \r <Action>(ReformatCode)
"" Map <leader>d to start debug
"map <leader>d <Action>(Debug)
"" Map \b to toggle the breakpoint on the current line
"map \b <Action>(ToggleLineBreakpoint)

" Unmap common Ctrl combinations
"unmap <C-p>
"unmap <C-n>
"unmap <C-f>
"unmap <C-r>
"unmap <C-a>
"unmap <C-d>

