# Leela Master Weight
Leela Master weight is training from leela zero self-play sgf and human sgf file, since it too big, I will upload weight file to 

https://drive.google.com/drive/folders/1bB8ee1wFuRWL9nPhsl4_BPUhcWSBuxO0?usp=sharing

Leela Master E is 10*128 network(complete)

Leela Master W is 20*128 network(complete)

Leela Master G is 15*192 network(Last is LeelaMaster_G13)

Welcome to our discuss qq group: 693862763

# About human sgf 
The human sgf is mainly download from https://github.com/yenw/computer-go-dataset

I used AI, Professional, TYGEM, Tom and CGOS game, mix with leelazero sgf.

# About G-serial

G01 - G03 : 90% leelazero sgf + 10% human style game

G04 - G08 : 80% leelazero sgf + 20% human style game

G09 - G13 : 70% leelazero sgf + 30% human style game

The training set is keeping change by random sample for each 256k step.

And I will keep to increase human style game percent to see when the strength of weight will decent, and in our test, the style of leela master weight changed very frequently between each weight, and the strength is almost same. So you can test each weight to find the style you love.

# About W/E-serial
W/E-serial is training with 70% human style game + 30% leelazero sgf, the strength is equal to same network size of last leela-zero.
