# FluidStride-Website

## Install `jekyl`

1. Install `rvm`

#### Ubuntu
Install [`ubuntu_rvm`](https://github.com/rvm/ubuntu_rvm)
```bash
sudo apt-get install software-properties-common
# Run next few lines in new terminal
sudo apt-add-repository -y ppa:rael-gc/rvm
sudo apt-get update
sudo apt-get install rvm
```

If you get `unable to locate package`, check if the package is available for your version.
```bash
cat /var/lib/apt/lists/ppa.launchpad.net_rael-gc_*_Packages | grep "Package:" | sort | uniq
```

#### macOS
Install [`rvm`](https://rvm.io/rvm/install)
```bash
\curl -sSL https://get.rvm.io | bash -s stable --ruby
```

#### macOS
Install [`rvm`](https://rvm.io/rvm/install)
```bash
\curl -sSL https://get.rvm.io | bash -s stable --ruby
```

2. Open new terminal and install `ruby`
```bash
rvm list known
rvm install 2.5.0
rvm use 2.5.0
```

3. Install `jekyl`
```bash
gem install jekyll bundler
```

4. Install `Gemfile`
```bash
bundle install
```

Note: you may have issues with `openssl` for compiling Ruby gems from source. This
can be solved by running `brew info openssl` and following the provided instructions
to allow compilers to find `openssl`.

## Local Development
```bash
# Launches site on localhost:4000
bundle exec jekyll serve --livereload
```

## Updating Assets
- **Note:** use absolute paths like `app_icon: /assets/appicon.png` in `_config.yml`

# Credits
- Jekyll
- FontAwesome
- [emilbaehr/automatic-app-landing-page](https://github.com/emilbaehr/automatic-app-landing-page)
