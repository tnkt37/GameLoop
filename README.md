GameLoop  
========  
  
C#でゲームループを回すためのクラス  
動作は呼び出し元(GameStart()したスレッド)とは別のスレッドで動作します  
.NETの命名規則を無視していたりそもそも設計がひどかったりであまりオススメできません。    
  
使い方:  
  
TNKTLib.FPSTimer timer = new FPSTimer();  
timer.Fps = 30;  
timer.GameInit += () => {};//初期化処理を追加。他のイベントもこれと同じ型  
timer.GameUpdate += timer_GameUpdate;//毎フレーム呼び出される更新処理を追加  
timer.GameRender += timer_GameRender;//描画処理を追加  
timer.GameStart();  
