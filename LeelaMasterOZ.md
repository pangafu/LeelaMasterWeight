# About Leela Master OZ-Serial
OZ serial is start from all-zero network, has some special supervisor-training parameter:

1. Traning color plan:(thanks @alreadydone @Hersmunch) 

   Color plan can be used for handicape game, please refer to 
   
   a. https://github.com/gcp/leela-zero/issues/1599 
   
   b. https://github.com/gcp/leela-zero/pull/1825
   
   c. https://github.com/alreadydone/lz/tree/stm4komi
   
2. Split traning. (thanks @icee)

   After compare GX-Serial, it seems that zero sgf is good at opening and human is good at ending game, so I split the traning data, and use more zero data at opening game, more human data at ending game.
   
3. Balance training.

   The 80%  exist go sgf is end before 200 step, so the traning data is poor after 200 step. I sampling more at ending game to balance traning.
   
It highly recommend use OZ-serial network with @alreadydone komi version leelazero branch:
   
   https://github.com/alreadydone/lz
   
   branch: komi+batch, komi+next, komi+tensorbatch, komi ....


Please enjoy the different go game style.

# About Training Data
Training Data has contain bellow datas.

1. Leela Training Set Data: from https://leela.online-go.com/training/ (last 150W games)
   
   Data use to make netowkr's PN, VN more accurate at komi 7.5. 
   
   NOTE: I don't modify the Leela Training Set Data's color plan to other value, because the traning data's VN is mostly come from the percent of wining game, and I have no idea to filter the game by STM color.
   
2. Human games: https://github.com/yenw/computer-go-dataset (about 100W games)

3. Leela match games: https://leela.online-go.com/zero/all_match.sgf.xz  (last 20W games)

4. Octopus self-play games(about 100W games)
   
   The 2,3,4 datas is dumped to 7.5 and other komi games.
  
# About komi data dump

When dump data from sgf, I use rule bellow to dump komi data:

1. Filter all W+R, B+R games, the games left only W+N.n and B+N.n;

2. All games is make in 7.5 komi, so if a game is W+2.5, when komi set to 7.5, 8.5, 9.5, the white side is still win, so I can make komi<10 data with this game. If a game is B+2.5, when komi set to 7.5, 6.5, 5.5, the black side can still win, so I can make komi>5 data with this game.

And I dump many komi data in [-30, 40], each komi point had right distribution of black and white win games, so the VN value maybe training right in each komi value.


# About Split training & balance training
@icee make a tool to split training data to different part by step number, we can use this tools to split the training data to [0-30), [30-100),[100-200),[200-300),[300-999]

So we get many training data with different step part, Now we can sample the data we love from the data, I made a tools to sample the data:

1. Split sample: After compare GX-Serial, it seems that zero sgf is good at opening and human is good at ending game, so I split the traning data, and use more zero data at opening game, more human data at ending game.
   
2. Balance sample: The 80%  exist go sgf is end before 200 step, so the traning data is poor after 200 step. I sampling more at ending game to balance traning.

Also I sample more komi data at the first 30 steps, sample less down in left part....





