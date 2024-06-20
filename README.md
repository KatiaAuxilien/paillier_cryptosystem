<h1 align="center">Welcome to Cryptosystem Pailler images 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-1-blue.svg?cacheSeconds=2592000" />
</p>

> Program to encrypt and decrypt images (.pgm) with Paillier cryptosystem.
> Repository dedicated to an internship in the ICAR team at LIRMM.

📄 [Documentation](https://katiaauxilien.github.io/encryption_images_Paillier/html/) *in progress*

## Installation


Firstly, you need to clone or download the project. Through your usage, we recommend to `git pull` to update the project.

Then, install `g++` version 11.
```sh
$ sudo apt install g++-11
```

You maybe need to install `make`, so use the command :
```sh
$ sudo apt install make
```
In order that you can compile to each modification, they have at your proposal the `make` programs in folders `main`, use the command :
```sh
$ make -f [makefile]
```

## Usage

### Encryption
```sh
$ ./Paillier_pgm_main.out encryption [ARGUMENTS] [FILE.PGM]
```
```sh
$ ./Paillier_pgm_main.out encrypt [ARGUMENTS] [FILE.PGM] 
```
```sh
$ ./Paillier_pgm_main.out enc [ARGUMENTS] [FILE.PGM]
```
```sh
$ ./Paillier_pgm_main.out e [ARGUMENTS] [FILE.PGM]
```

### Decryption

```sh
$ ./Paillier_pgm_main.out decryption [PRIVATE KEY FILE .BIN] [FILE.PGM] [ARGUMENTS]
```

```sh
$ ./Paillier_pgm_main.out decrypt [PRIVATE KEY FILE .BIN] [FILE.PGM] [ARGUMENTS]
```

```sh
$ ./Paillier_pgm_main.out dec [PRIVATE KEY FILE .BIN] [FILE.PGM] [ARGUMENTS]
```
```sh
$ ./Paillier_pgm_main.out d [PRIVATE KEY FILE .BIN] [FILE.PGM] [ARGUMENTS] 
```

The image to encrypt or to decrypt can be specify after the key or the options, or at the end.

### Options
#### P and Q

```sh
$ ./Paillier_pgm_main.out encryption [p] [q] [FILE.PGM] 
```

Encryption mode where you specify p and q arguments. p and q are prime number where pgcd(p * q,p-1 * q-1) = 1.

#### Keys
`-k` or `-key` to specify usage of private or public key, followed by `file.bin`, your key file.

Encryption mode where you specify your public key file with format `.bin`.
```sh
$ ./Paillier_pgm_main.out encryption -k [PUBLIC KEY FILE .BIN] [FILE.PGM] 
```
```sh
$ ./Paillier_pgm_main.out encryption -key [PUBLIC KEY FILE .BIN] [FILE.PGM]
```

Decryption mode where you specify your private key with format `.bin`.
The option ``-k` is optional, because it's obligatory to specify private key at decryption.
```sh
$ ./Paillier_pgm_main.out decryption -k [PRIVATE KEY FILE .BIN] [FILE.PGM]
```

#### Others

`-distribution` or `-distr` ou `-d` to split encrypted pixel on two pixel.

`-histogramexpansion` ou `-hexp` to specify during **encryption** that we want to transform the histogram befor image encryption.

`-optlsbr` or `-olsbr` to specify that we want to use bit compression with encrypted through optimized r generation.

WARNING : You can't combine `-distribution` and `-optlsbr`, if you do that the priority is `-optlsbr`.

<!-- 
\verb|-optlsbrcomp| ou \verb|-olsbrc|  pour préciser qu'on souhaite utiliser la "compression" des pixels chiffrés en générant des valeurs aléatoires \(r\) favorable et en utilisant des compléments de chiffré pour élargir les valeurs.\\

\verb|-optlsbrg| ou \verb|-olsbrg|  pour préciser qu'on souhaite effectuer une "compression" des pixels chiffrés en générant des valeurs aléatoires \(r\) favorable et en générant le paramètre \(g\) le plus optimisé pour favoriser cette compression.\\
… -->

## Progression

- [X] Add a -help -h option to print user's guide.
- [X] Generate documentation with dioxygen. 
  - [ ] Complete documentation. [*in progress*]
- [X] Implement LSB compression.
- [ ] Implement new solution for size encryption. (to make program usable with n > 256)

## Author

👤 **Auxilien Katia**

* Website: https://katiaauxilien.github.io/
* Github: [@KatiaAuxilien](https://github.com/KatiaAuxilien)
* LinkedIn: [@katia-auxilien](https://linkedin.com/in/katia-auxilien)

**Supervised by William PUECH**

* Website: https://www.lirmm.fr/~wpuech/

**Based on Norman HUTTE's and Bianca JANSEN VAN RENSBURG's code**

## Show your support

Give a ⭐️ if this project helped you!

## 📝 License

Copyright © 2024 Katia Auxilien.
This project is MIT licensed.


***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
