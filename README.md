# Resume

This repository contains the LaTeX source for the resume in `resume.tex`.

## Install Tectonic

Tectonic is a self-contained TeX/LaTeX engine that downloads required support
files automatically, so you do not need a full TeX Live installation.

### macOS or Linux

Install with the official shell installer:

```sh
curl --proto '=https' --tlsv1.2 -fsSL https://drop-sh.fullyjustified.net | sh
```

The installer places the `tectonic` executable in the current directory. Move it
to a directory on your `PATH`, for example:

```sh
mkdir -p "$HOME/.local/bin"
mv tectonic "$HOME/.local/bin/"
```

Make sure `$HOME/.local/bin` is on your `PATH`.

### Homebrew

If you use Homebrew:

```sh
brew install tectonic
```

### Conda

If you use Conda:

```sh
conda install -c conda-forge tectonic
```

### Verify Installation

```sh
tectonic --version
```

## Compile the Resume

From the repository root, run:

```sh
tectonic -X compile resume.tex
```

This compiles `resume.tex` and writes the output PDF to:

```text
resume.pdf
```

On the first run, Tectonic may download LaTeX packages and support files. Later
runs should be faster because those files are cached.

## Clean Generated Files

Tectonic normally keeps the repository clean and only writes the final PDF. If
you compile with options such as `--keep-intermediates`, remove generated
temporary files before committing.

## References

- Tectonic install documentation: <https://tectonic-typesetting.github.io/book/latest/installation/>
- Tectonic compile command: <https://tectonic-typesetting.github.io/book/latest/v2cli/compile.html>
