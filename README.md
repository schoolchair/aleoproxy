建議在ubuntu 22.04執行  aleoproxy, 如果使用ubuntu Server + GPU挖礦，可以直接在該Server上執行，執行格式如下：
./aleoproxy local_port remoe_port remote_ip &
local_port: 對挖礦程式/礦機提供的服務端口，
remote_port:: 國外中轉主機的服務端口, remoe_ip 國外中轉主機的IP

例如你執行aleoproxy 在IP 為8.8.8.8的主機上，那麽按如下方式執行
./aleoproxy 8888 16888 8.8.8.8 &
在礦機上就應該這樣設置：
stratum+tcp://8.8.8.8:8888
另外在國外IP8.8.8.8的主機上，應該執行中轉返水程式
./aleorebate 16888 rebate_account &

注意這裏8.8.8.8只是參考，不是真實的中轉返水主機的IP



中轉返水程式
在國外服務器上安裝，按一下格式執行. 
./aleorebate local_port rebate_account 0 &  （單機執行，不加密）
在魚池挖礦程式裏直接設置挖礦中轉服務器為本機的IP及local_port

上述兩個程式，aleoproxy是傳輸加密的，不是一定需要執行，但是中轉返水程式必須使用，才能實現邊中轉邊返水的目的
有自己服務器的可以按以上説明自己執行中轉返水程式，拿到可觀的返水

沒有中轉服務的小散可以使用以下的格式設置(不提供返水服務)
stratum+tcp://3.25.59.169:50010

有一定數量機器的礦場可以按上述説明自己架server運行上面的程序，或者我們可以協助架設。也可以洽談由我們提供專用通道。
telegram @bitgoldcash
