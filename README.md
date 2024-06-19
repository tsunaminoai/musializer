<!-- gen-readme start - generated by https://github.com/jetify-com/devbox/ -->
## Getting Started
This project uses [devbox](https://github.com/jetify-com/devbox) to manage its development environment.

Install devbox:
```sh
curl -fsSL https://get.jetpack.io/devbox | bash
```

Start the devbox shell:
```sh 
devbox shell
```

Run a script in the devbox environment:
```sh
devbox run <script>
```
## Scripts
Scripts are custom commands that can be run using this project's environment. This project has the following scripts:

* [build](#devbox-run-build)
* [clean](#devbox-run-clean)
* [run](#devbox-run-run)
* [test](#devbox-run-test)
* [test-watch](#devbox-run-test-watch)

## Shell Init Hook
The Shell Init Hook is a script that runs whenever the devbox environment is instantiated. It runs 
on `devbox shell` and on `devbox run`.
```sh
echo 'Welcome to devbox!'
devbox run
```

## Packages

* [zig@0.12.0](https://www.nixhub.io/packages/zig)
* [zls@latest](https://www.nixhub.io/packages/zls)
* [watchexec@latest](https://www.nixhub.io/packages/watchexec)

## Script Details

### devbox run build
```sh
zig build
```
&ensp;

### devbox run clean
```sh
rm -rf zig-out zig-cache
```
&ensp;

### devbox run run
```sh
zig build run
```
&ensp;

### devbox run test
```sh
zig build test
```
&ensp;

### devbox run test-watch
```sh
watchexec --exts zig --watch src 'clear && zig build test'
```
&ensp;



<!-- gen-readme end -->
