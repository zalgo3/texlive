# TeX Live Docker image
## About
- Docker image including relatively minimal TeX Live packages.
- Add some packages to [arcatdmz/texlive](https://github.com/arcatdmz/texlive) to be useful for mathematical scientists who use Japanese and English.

## Build

```bash
$ docker build -t zalgo3/texlive .
```

## Pull

```bash
$ docker pull zalgo3/texlive
```

## Compile LaTeX files
### platex

```bash
$ docker container run -v $(pwd):/texsrc -it --rm zalgo3/texlive platex foo.tex
```

### latexmk

```bash
$ docker container run -v $(pwd):/texsrc -it --rm zalgo3/texlive latexmk -pvc foo.tex
```
