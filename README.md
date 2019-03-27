# Leela Master Weight
Leela Master weight is training from leela zero self-play sgf and human sgf file, since it too big, I will upload weight file to 

https://drive.google.com/drive/folders/1bB8ee1wFuRWL9nPhsl4_BPUhcWSBuxO0?usp=sharing


Leela Master OZ is 30*256 network(last is OZ17)

Leela Master E is 10*128 network(complete)

Leela Master W is 20*128 network(complete)

Leela Master G/GX is 15*192 network(complete)

Leela Zero Z is 30*256 network(complete)

Leela Master B is 30*256 network(complete)

Welcome to our discuss qq group: 693862763

# About LeelaMaster strength (ELO)

Go AI Ratings (by @breakwa11)

https://github.com/breakwa11/GoAIRatings

Home-made Elo ratings for some engines (by xela@lifein19x19.com)

https://lifein19x19.com/viewtopic.php?f=18&t=16086

Strength of the Leela Master G13:

http://zero.sjeng.org/match-games/5b26c77d48e3e5462acf0c4a


# About leelazero sgf 
LeelaZero Homepage : http://zero.sjeng.org/

LeelaZero Github: https://github.com/gcp/leela-zero

LeelaZero Training set: https://leela.online-go.com/training/

LeelaZero sgf pack: http://sjeng.org/zero


# About human sgf 
The human sgf is mainly download from https://github.com/yenw/computer-go-dataset

I used AI, Professional, TYGEM, Tom and CGOS game, mix with leelazero sgf.


# About handicap game（关于让子棋）
It report that GX37/GX38 - GX6x serial suit for handicap game with komi version leelazero by @alreadydone ~ So you can try handicap games by GX37 or newer.

Thread: https://github.com/gcp/leela-zero/issues/1599 

komi version leelazero(by @alreadydone): https://github.com/alreadydone/lz/tree/komi

release version: https://github.com/alreadydone/lz/releases

[0308 updated] OZ-serial with komi engine(white) vs zen7(black), can handicap 4 stone and komi 0
[0327 updated] upload LeelaZero_DKomi+Filter to google share folder, if you can read chinese, you can setup a very powerful hadicape engine.


# About OZ-serial
OZ-serial is awesome in komim mode , in my test , OZ13 with komi engine(white) vs zen7(black), can handicap 4 stone and komi 0

OZ serial is start from all-zero network, has some special supervisor-training parameter:

1. Traning color plan:(thanks @alreadydone @Hersmunch) 

   Color plan can be used for handicape game, please refer to 
   
   a. https://github.com/gcp/leela-zero/issues/1599 
   
   b. https://github.com/gcp/leela-zero/pull/1825
   
   c. https://github.com/alreadydone/lz/tree/stm4komi
      https://github.com/Hersmunch/leela-zero/tree/komi
   
2. Split traning. (thanks @icee)

   After compare GX-Serial, it seems that zero sgf is good at opening and human is good at ending game, so I split the traning data, and use more zero data at opening game, more human data at ending game.
   
3. Balance training.

   The 80%  exist go sgf is end before 200 step, so the traning data is poor after 200 step. I sampling more at ending game to balance traning.
   
It highly recommend use OZ-serial network with @alreadydone @Hersmunch komi version leelazero branch:
   
   https://github.com/Hersmunch/leela-zero/tree/komi
   
   https://github.com/alreadydone/lz
   branch: komi+batch, komi+next, komi+tensorbatch, komi ....


Please enjoy the different go game style. 

More detail please see https://github.com/pangafu/LeelaMasterWeight/blob/master/LeelaMasterOZ.md
   

# About GX-serial

GX1x is 10% human style game

GX2x is 20% human style game

GX3x is 30% human style game

GX4x is 40% human style game 

GX5x is 50% human style game 

GX6x is 60% human style game 

GX7x is 70% human style game 

GX8x is 80% human style game 

GX9x is 90% human style game 

GXAx is 100% human style game 


And I will keep to increase human style game percent to see when the strength of weight will decent, and in our test, the style of leela master weight changed very frequently between each weight, and the strength is almost same. So you can test each weight to find the style you love.

# About W/E-serial
W/E-serial is training with 70% human style game + 30% leelazero sgf,

the strength is equal to same network size of leela-zero.


# About G-serial
G Serial now merged into GX Serial

G01 - G03 : 90% leelazero sgf + 10% human style game

G04 - G08 : 80% leelazero sgf + 20% human style game

G09 - G13 : 70% leelazero sgf + 30% human style game

The training set is keeping change by random sample for each 256k step.


# About B-serial
B-serial is traing from leelazero + human sgf in 30 * 256 network size, it based on z-serial network.

B01 - B03 : 80% leelazero sgf + 20% human style game

Current learning rate is 0.0005


# About Z-serial
Z-serial is training from leelazero sgf in 30 * 256 network size.

The last learning rate is 0.0005, and the traning set is random sample from leela zero's last 3,000,000 games

Z-serial's end network is used to make B-serial.



# About Octopus (章鱼围棋)
Octopus go another way to make human style AI, we will try some different techology and some new idea, it not same with leela master, and it will opensource when ready.

章鱼围棋会用另外一条思路去做人谱AI， 会采用一些新的技术和尝试一些新的想法，请不要用leelamaster的棋力去衡量章鱼围棋，当整个成熟后，会考虑开源。
