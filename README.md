# Setup CrossLang

This is the action for setting up my programming language [CrossLang](https://crosslang.tesseslanguage.com/)


Github actions example

```yaml
name: GitHub Actions Demo
run-name: ${{ github.actor }} is testing out GitHub Actions 🚀
on: [push]

jobs:
  build-and-push-image:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Install CrossLang
        uses: tesses50/setup-crosslang@v1
      - name: Build and Push
        run: |
          crosslang build
          crosslang upload-package --token="${{ secrets.CPKG_KEY }}" --host="https://cpkg.tesseslanguage.com/"
```


Gitea Actions example
```yaml
name: Gitea Actions Demo
run-name: ${{ gitea.actor }} is testing out Gitea Actions 🚀
on: [push]

jobs:
  build-and-push-image:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Install CrossLang
        uses: https://git.tesses.org/tesses50/setup-crosslang@v1
      - name: Build and Push
        run: |
          crosslang build
          crosslang upload-package --token="${{ secrets.CPKG_KEY }}" --host="https://cpkg.tesseslanguage.com/"
```