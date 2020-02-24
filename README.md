# 009Music-Player
VideoView SeekBar 自定義View(音頻條)<br />


<img src="https://github.com/tzutzu858/ChallengeDailyUI/blob/master/Day01_10/09_Music%20Player/mediaPlayer.gif" width="350" >
<br /><br /><br />

### bug修正<br />
<img src="https://github.com/tzutzu858/009Music-Player/blob/master/1.png" width="350" >
<br /><br />

把mMediaPlayer.stop();後再去動seekBar , 程式會shut down<br />
錯誤:IllegalStateException<br />
stop後必須再執行 prepareAsync() 或 prepare() 才能重新播放。<br />
但不可能在seekBar裡放prepareAsync() 或 prepare()<br />
UX角度思考,音樂都關掉了還可以一直動seekBar也很奇怪<br />
所以直接讓使用者按下stop鍵時<br />
讓seekBar.setVisibility(View.VISIBLE);<br />
是有一點鴕鳥心態的fu啦Σ( ° △ °|||)<br />
