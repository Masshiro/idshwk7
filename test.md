### Description of Detailed Process to Hide Information into A Digital Picture

#### Set-up

- First, we need to find a reliable tool to help us to achieve the goal, which eventually we choose this [LSB-Steganography](https://github.com/RobinDavid/LSB-Steganography).
- Next, we need to download the project files from the repository.
- Following the usage guide in that page, we still have to download some dependencies which are listed in file `requirements.txt`, and to install those by applying command `pip install -r requirements.txt`.



#### How to hide information

##### Required files:

- `TokyoTower.png`, the carrier picture which holds the information, aka the original picture. 
- `secret.md`, the pure text containing the information we'd like to conceal. 
- `LSBSteg.py`, whose partial functions are used to achieve our goal.

##### Command 

Use following command to hide information:

```python
$ python3 LSBSteg.py encode -i TokyoTower.png -o test.png -f secret.md 
```



#### How to recover hidden information

##### Required files:

- `test.png`, the main part of this homework, which contains the secret and original picture both. 
- `LSBSteg.py`, whose other parts of functions are used to extract the secret.

##### Command

Use following command to extract secret from the picture:

```python
$ python3 LSBSteg.py decode -i test.png -o recovered.txt
```



#### Reference

- https://github.com/RobinDavid/LSB-Steganography

