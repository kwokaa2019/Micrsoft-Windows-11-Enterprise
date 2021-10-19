Micrsoft Windows 11 Enterprise  90 天評估版轉換為 Windows 11 Enterprise LTSC

首先去微軟官方載網站，下載 Micrsoft Windows 11 Enterprise LTSC 評估版

https://www.microsoft.com/zh-tw/evalcenter/evaluate-windows-11-enterprise

Windows 11 LTSC 企業評估版iso「光碟映像檔」下載

https://software-download.microsoft.com/download/sg/22000.194.210913-1444.co_release_svc_refresh_CLIENTENTERPRISEEVAL_OEMRET_x64FRE_zh-tw.iso


安裝好系統後，你可以檢查指令 systeminfo 可以發現當前是評估版本


我們需要下載版本檔案放入對應資料夾</p>
<blockquote><p>Windows 10 LTSC Sku Files</p>
<p>下載 : <a target="_blank" rel="nofollow" href="https://gitlab.com/x8602222/windows-10-ltsc-sku-files/-/blob/main/skus.zip">Gitlab </a>、<a target="_blank" rel="nofollow" href="https://mega.nz/file/xZkATCZT#nELU8sW4SwDgkn9qm0ZP-m5CS7jsdDXpylARDM3rRMM">MEGA</a></p></blockquote>
<p>放置路徑 <code>C:\Windows\System32\spp\tokens\skus

接下來使用管理員執行CMD</p>
<p><img loading="lazy" class="alignnone size-full wp-image-28486" src="https://www.gdaily.org/wp-content/uploads/2021/10/01.png" alt="" width="800" height="666" /></p>
<p>&nbsp;</p>
<p>執行以下指令，大致上是切換讀取的授權檔案，卸載當前金鑰，安裝LTSC金鑰(無法啟動但可以切換版本)</p>
<pre style="color: #d1d1d1; background: #000000;">cscript.exe %windir%<span style="color: #d2cd86;">\</span>system32<span style="color: #d2cd86;">\</span>slmgr.vbs <span style="color: #d2cd86;">/</span>rilc
cscript.exe %windir%<span style="color: #d2cd86;">\</span>system32<span style="color: #d2cd86;">\</span>slmgr.vbs <span style="color: #d2cd86;">/</span>upk <span style="color: #d2cd86;">&gt;</span><span style="color: #e66170; font-weight: bold;">nul</span> <span style="color: #00a800;">2</span><span style="color: #d2cd86;">&gt;</span><span style="color: #d2cd86;">&amp;</span><span style="color: #00a800;">1</span>
cscript.exe %windir%<span style="color: #d2cd86;">\</span>system32<span style="color: #d2cd86;">\</span>slmgr.vbs <span style="color: #d2cd86;">/</span>ckms <span style="color: #d2cd86;">&gt;</span><span style="color: #e66170; font-weight: bold;">nul</span> <span style="color: #00a800;">2</span><span style="color: #d2cd86;">&gt;</span><span style="color: #d2cd86;">&amp;</span><span style="color: #00a800;">1</span>
cscript.exe %windir%<span style="color: #d2cd86;">\</span>system32<span style="color: #d2cd86;">\</span>slmgr.vbs <span style="color: #d2cd86;">/</span>cpky <span style="color: #d2cd86;">&gt;</span><span style="color: #e66170; font-weight: bold;">nul</span> <span style="color: #00a800;">2</span><span style="color: #d2cd86;">&gt;</span><span style="color: #d2cd86;">&amp;</span><span style="color: #00a800;">1</span>
cscript.exe %windir%<span style="color: #d2cd86;">\</span>system32<span style="color: #d2cd86;">\</span>slmgr.vbs <span style="color: #d2cd86;">/</span>ipk M7XTQ<span style="color: #d2cd86;">-</span>FN8P6<span style="color: #d2cd86;">-</span>TTKYV<span style="color: #d2cd86;">-</span>9D4CC<span style="color: #d2cd86;">-</span>J462D
</pre>
<p><img loading="lazy" class="alignnone size-full wp-image-28487" src="https://www.gdaily.org/wp-content/uploads/2021/10/02.png" alt="" width="800" height="600" /></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>切換後先重啟系統，讓系統重新辨識版本，否則systeminfo仍是評估版</p>
<p>重啟後執行cmd的<code>systeminfo</code>已經可以確認切換版本</p>
<p><img loading="lazy" class="alignnone size-full wp-image-28488" src="https://www.gdaily.org/wp-content/uploads/2021/10/04.png" alt="" width="800" height="600" /></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>當然這邊還是未授權的狀態</p>
<p>接下來看大家是自己有序號還是透過數位授權工具來啟動都可以啦，請依照自己的方式啟動系統</p>


  
  
  
  
  
  
  
  
  
  


93MGM-NTFKD-6BK63-R6FYR-6Q9PB
