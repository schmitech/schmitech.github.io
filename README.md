# Schmitech Website

This repository contains the Jekyll-based website for Schmitech. The site is built using Jekyll and hosted on GitHub Pages.

## Prerequisites

### Install Homebrew
Ensure you have Homebrew installed. If not, install it by running:
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Install rbenv and Ruby

1. **Install rbenv**:
```sh
brew install rbenv
brew install ruby-build
```

2. **Configure rbenv**:
Add to your shell configuration file (e.g., `~/.zshrc`, `~/.bash_profile`, or `~/.profile`):
```sh
export PATH="$HOME/.rbenv/bin:$PATH"
eval "$(rbenv init -)"
```

3. **Reload your shell configuration**:
For zsh:
```sh
source ~/.zshrc
```
For bash:
```sh
source ~/.bash_profile
```

4. **Install Ruby**:
```sh
rbenv install 3.3.6
rbenv global 3.3.6
```

5. **Verify the installation**:
```sh
ruby -v
which ruby  # Should point to ~/.rbenv/shims/ruby
```

### Troubleshooting Ruby Installation

If you encounter Ruby version issues:

1. **Check rbenv initialization**:
```sh
type rbenv  # Should output: "rbenv is a function"
```

2. **Verify rbenv shims**:
```sh
rbenv versions  # Should list installed versions
```

3. **Check PATH configuration**:
```sh
echo $PATH  # ~/.rbenv/shims should be at the beginning
```

4. **Rehash rbenv**:
```sh
rbenv rehash
```

## Install Jekyll and Dependencies

1. **Install Jekyll and Bundler**:
```sh
gem install jekyll bundler
```

2. **Install project dependencies**:
```sh
bundle install
```

## Local Development

1. **Clone the repository**:
```sh
git clone https://github.com/schmitech/schmitech.github.io.git
cd schmitech.github.io
```

2. **Run the site locally**:
```sh
bundle exec jekyll serve
```

The site should now be running at `http://localhost:4000`

## Common Tasks

### Clean up and rebuild
```sh
# Remove generated files
bundle exec jekyll clean

# Rebuild the site
bundle exec jekyll build
```

### Update dependencies
```sh
bundle update
```

### Add new pages
Create new .md files in the root directory with the following front matter:
```yaml
---
layout: page
title: Your Page Title
permalink: /your-page-url/
---
```

### Add new service pages
Create new .md files in the `_services` directory with the following front matter:
```yaml
---
layout: page
title: Service Title
permalink: /services/service-name/
---
```

## Deployment

The site is automatically deployed to GitHub Pages when changes are pushed to the main branch. To deploy:

```sh
git add .
git commit -m "Your commit message"
git push origin main
```

## Bundler Issues

If you encounter bundler errors:
```sh
rm Gemfile.lock
bundle install
```

## Contributing

1. Create a new branch for your changes
2. Make your changes
3. Test locally
4. Submit a pull request

## Support

For questions or issues, please contact info@schmitech.ai