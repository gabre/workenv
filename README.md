# Good programs

- zellij
- fd find
- rgrep
- glow
- atuin

# LazyVim

The command `:terminal` opens a new terminal. In the different (horizontal or vertical) windows, one can display the terminal or any file.

Use the following snippet to configure Telescope to show hidden files in find/grep (.config/nvim/lua/plugins/files.lua):
```
return {
  {
    "nvim-neo-tree/neo-tree.nvim",
    opts = {
      filesystem = {
        filtered_items = {
          visible = true,
          show_hidden_count = true,
          hide_dotfiles = false,
          hide_gitignored = true,
          hide_by_name = {
            -- '.git',
            -- '.DS_Store',
            -- 'thumbs.db',
          },
          never_show = {},
        },
      },
    },
  },
  {
    "nvim-telescope/telescope.nvim",
    opts = {
      defaults = {
        vimgrep_arguments = {
          "rg",
          "--color=never",
          "--no-heading",
          "--with-filename",
          "--line-number",
          "--column",
          "--smart-case",
          "--hidden", -- thats the new thing
        },
      },
      pickers = {
        find_files = {
          file_ignore_patterns = {
            -- "node_modules", ".git", ".venv"
          },
          hidden = true,
        },
      },
    },
  },
}
```

Use the `:cd ~` command to set the "cwd" to home (then Space+E will open a file browser/tree there).
