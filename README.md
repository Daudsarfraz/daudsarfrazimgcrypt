# daudsarfrazimgcrypt

A CLI that encrypts and decrypts png, jpg, jpeg images to a gibberish image and provides you the key to unlock it later so that you have the complete control of your images.

## Installation

```sh
npm i -g daudsarfrazimgcrypt
```

## Usage

```sh
daudsarfrazimgcrypt <command> [option]
```

or run it directly using npx

```sh
daudsarfrazimgcrypt <command> [option]
```

### commands

```sh
help  #prints help info
```

### options

```sh
  -e, --encrypt              # The image to encrypt
  -d, --decrypt              # The image to decrypt
  -c, --clear                # Clear the console Default: false
  --noClear                  # Don't clear the console Default: true
  -v, --version              # Print CLI version Default: false
  -k, --key                  # The key to use for decryption Default: false
  -i, --outputImageFileName  # The output image
  -p, --outputKeyFileName    # The output key
```

## examples

Command

### For encrypting an image myImage.png to encryptedImage.png and saving the key to key.txt

```sh
daudsarfrazimgcrypt -e img.png -i encryptedImageName.png -p keyFile.txt
```

output

```sh
 daudsarfrazimgcrypt  v0.0.1 by daudsarfraz
An image encryption node-js cli

✔ Image read successfully
✔ Output image file name is valid
✔ Output key file name is valid
✔ Image data read successfully
✔ Key generated successfully
✔ Image encrypted successfully
✔ Image saved successfully
✔ Key saved successfully

✔  Image encrypted successfully  Image encrypted successfully:
                                  Encrypted image: encryptedImageName.png
                                  Key: keyFile.txt

 Give it a star on github:  https://github.com/Daudsarfraz/daudsarfrazimgcrypt
```

### For decrypting an image encryptedImage.png with its key key.txt to decryptedImage.png

```sh
daudsarfrazimgcrypt -d encryptedImage.png -k key.txt -i decryptedImage.png
```

output

```sh
 imcrypt  v0.0.1 by theninza
An image encryption node-js cli

✔ Image read successfully
✔ Key read successfully
✔ Decryption successful
✔ Image saved successfully

✔  Success  Image decrypted successfully

                        Decrypted Image: decryptedImage.png

 Give it a star on github:  https://github.com/Daudsarfraz/daudsarfrazimgcrypt
```

## Limitations

While encryption and decryption is perfect on the png images. On jpg and jpeg, the operation is not perfect. Jpg and jpeg images are lossy and while encryption and decryption, a few pixels values are changed. The decrypted image is however, very similar to the original image but with a few pixels changed.
