# FluidStride-Website

## Install `jekyl`

1. Install `rvm`

#### Ubuntu
Install [`ubuntu_rvm`](https://github.com/rvm/ubuntu_rvm)
```bash
sudo apt-get install software-properties-common
sudo apt-add-repository -y ppa:rael-gc/rvm
sudo apt update
sudo apt install rvm
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
