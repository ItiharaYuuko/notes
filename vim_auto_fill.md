# Vim Auto Fill Function Installation

* Vim editor software installation
    1. Windows binary files installer for download [gvim_8.2.2825.exe](https://github.com/vim/vim-win32-installer/releases/download/v8.2.2825/gvim_8.2.2825_x86_signed.exe)
    2. Download vim source code to manual install [vim-8.1.tar.bz2](ftp://ftp.vim.org/pub/vim/unix/vim-8.1.tar.bz2)
    3. Clone repo from github to compile and install
        ```bash
        $ git clone https://github.com/vim/vim.git
        $ cd vim
        $ sudo make
        $ sudo make install
        ```
        
* Nodejs framework installation
    1. On Linux (base Debian) `> sudo apt install nodejs`
    2. On Windows [Nodejs 16.13.2 LTS](https://nodejs.org/dist/v16.13.2/node-v16.13.2-x64.msi)
    3. Manual compile and install from source code [node-v16.13.2.tar.gz](https://nodejs.org/dist/v16.13.2/node-v16.13.2.tar.gz)
        ```bash
        $ tar -xf node-v16.13.2.tar.gz
        $ cd node-v16.13.2/
        $ ./configure
        $ sudo make
        ```

* NERDTree plugin for vims installation
    1. Create the vim theme folder
    2. Clone the github repo files to 
        ```bash
        $ cd ~/.vim/pack/vendor/start
        $ git clone https://github.com/scrooloose/nerdtree
        ```

    3. Append follow content to [^Vim profile] vim profile
        ```toml
        autocmd VimEnter * NERDTree | wincmd p

        autocmd BufEnter * if tabpagenr('$') == 1 && winnr('$') == 1 && exists('b:NERDTree') && b:NERDTree.isTabTree() | quit | endif

        nnoremap <C-n> :NERDTreeToggle<CR>
        ```

* vim-airline vim status bar beautify
    1. Clone the github repo files to [^Vim startup path]

* vim-one vim color matching for dark theme
    1. Clone the github repo files to [^Vim startup path]
    2. Config [^Vim profile] file appending follow content to apply settings
        ```toml
        set bg=dark
        colorscheme one
        ```

* coc.nvim plugin installing for code completion and syntax check
    1. Install Nodejs (version ≥ 10.12) 
        ```bash
        $ curl -sL install-node.now.sh/lts | bash
        ```
        *When installing Nodejs cannot connecting to server, or other unknown error occured please look above, install Nodejs manual.*

    2. Clone the github repo files to [^Vim startup path]
        ```bash
        $ git clone https://github.com/neoclide/coc.nvim.git
        ```

    3. Lunch the vim, and type below content and press enter to install the coc plugins
        ```bash
        $ :CocInstall coc-clangd
        $ :CocInstall coc-rust-analyzer
        $ :CocInstall coc-pyright
        ```

    4. Setting up completion and syntax checks time out and keymap
        *Append reference configuration [Example vim configuration](https://github.com/neoclide/coc.nvim#example-vim-configuration) code to [^Vim profile]*

****
[^Vim profile]: ~/.vimrc <!-- Vim configuration file. -->

[^Vim startup path]: ~/.vim/pack/vendor/start <!-- Storage the plugins files. -->