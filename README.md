# my_files
some sites to use that have decent free tiers right now

planetscale.com
vercel.com
back4app.com
upstash.com

# refreshes tmux config
unbind r
bind r source-file ~/.tmux.conf

# rebinds prefix
unbind-key C-b
set-option -g prefix C-v
bind-key C-a send-prefix

#act like vim 
setw -g mode-keys vi
bind-key h select-pane -L
bind-key j select-pane -D
bind-key k select-pane -U
bind-key l select-pane -R

# list of plugins
set -g @plugin 'tmux-plugin/tpm'
set -g @plugin 'christoomey/vim-tmux-navigator'
set -g @plugin 'dracula/tmux'

set -g @dracula-show-powerline-true
set -g @dracula-show-flags true
set -g @dracula-show-left-icon-session
set -g status-position top

# initialize TMUX plugin manager (must remain at the bottom of the config file)
run '~/.tmux/plugins/tpm/tpm'
