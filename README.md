# FluidStride-Website

## Install `jekyl`
1. Install [`rvm`](https://github.com/rvm/ubuntu_rvm)
```bash
sudo apt-get install software-properties-common
sudo apt-add-repository -y ppa:rael-gc/rvm
sudo apt update
sudo apt install rvm
```

2. Open new terminal and install `ruby`
```bash
rvm install 2.5.0
rvm use 2.5.0
```

3. Install `jekyl`
```bash
gem install jekyll bundler
```

## Local Development
```bash
# Launches site on localhost:4000
bundle exec jekyll serve --livereload
```

## Updating Assets
- **Note:** use absolute paths like `app_icon: /assets/appicon.png` in `_config.yml`
