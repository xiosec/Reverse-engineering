==============================================================================
            Sleepp v0.5 	by NEG
==============================================================================

 Only for OllyDbg v1.10


 1.Lowered CPU rate. 
 2.[Ctrl+Enter and Ctrl+D] moves to the selected data address. 
 3.When EIP indicates the code such as CALL EBX, Decode stack. 
 4.Patch to breakpoint bug. 


 [Translator  http://world.altavista.com/]
 1.Lowered CPU use rate.
 2.Ctrl+Enter and Ctrl+D which reduce CPU activity ratio, movement 
 3.EIP points to the cord/code of CALL EBX and the like to the address which the selective data indicates, decoding the argument in regard to stack 
 4. The correction patch is applied to the bug where the conditional statement of the conditional breakpoint becomes strange

 [original]
 1.デバッギーを走らせているときのCPU使用率を下げる
 2.Ctrl+EnterとCtrl+Dで、選択データが指し示すアドレスへ移動
 3.EIPが CALL EBX などのコードを指しているとき、スタック上の引数をデコード
 4.条件ブレークポイントの条件文がおかしくなるバグに修正パッチを当てる
