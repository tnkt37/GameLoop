GameLoop
========

C#でゲームループを回すためのクラス
動作は呼び出し元(GameStart()したスレッド)とは別のスレッドで動作します。

使い方:

FPSTimer timer = new FPSTimer();
timer.Fps = 30;
timer.GameUpdate += timer_GameUpdate;//毎フレーム呼び出される更新処理を追加
timer.GameRender += timer_GameRender;//描画処理を追加
timer.GameStart();
