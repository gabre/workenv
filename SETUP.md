# Use nvim as a vim alternative

╭─gabre@penguin ~/work/CLI_util_RSS_reader ‹main●›
╰─$ which nvim
/opt/nvim//nvim

╭─gabre@penguin ~/work/CLI_util_RSS_reader ‹main●›
╰─$ sudo update-alternatives --install /usr/bin/vim vim /opt/nvim/nvim 1111
update-alternatives: using /opt/nvim/nvim to provide /usr/bin/vim (vim) in auto mode

╭─gabre@penguin ~/work/CLI_util_RSS_reader ‹main●›
╰─$ update-alternatives --config vim
