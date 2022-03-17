
<p>&nbsp;</p>
<p>我們需要下載檔案</p>
<blockquote><p>Windows 10 LTSC Sku Files</p>
<p>下載 : <a target="_blank" rel="nofollow" href="https://gitlab.com/x8602222/windows-10-ltsc-sku-files/-/blob/main/skus.zip"  target="_blank" rel="noopener">Gitlab </a>、<a target="_blank" rel="nofollow" href="https://mega.nz/file/xZkATCZT#nELU8sW4SwDgkn9qm0ZP-m5CS7jsdDXpylARDM3rRMM"  target="_blank" rel="noopener">MEGA</a></p></blockquote>
<p>放置路徑 <code>C:\Windows\System32\spp\tokens\skus</code></p>
<p><img loading="lazy" class="alignnone size-full wp-image-28491" src="https://i.ibb.co/MsxH2CR/Virtual-Box-10-19-10-2021-16-35-12.png" alt="" width="1024" height="768" /></p>

<p>需要輸入的執行指令如下，大致上是切換讀取的授權檔案，卸載當前金鑰，安裝LTSC金鑰(無法啟動但可以切換版本)</p>
<pre style="color: #d1d1d1; background: #000000;">cscript.exe %windir%<span style="color: #d2cd86;">\</span>system32<span style="color: #d2cd86;">\</span>slmgr.vbs <span style="color: #d2cd86;">/</span>rilc
cscript.exe %windir%<span style="color: #d2cd86;">\</span>system32<span style="color: #d2cd86;">\</span>slmgr.vbs <span style="color: #d2cd86;">/</span>upk <span style="color: #d2cd86;">&gt;</span><span style="color: #e66170; font-weight: bold;">nul</span> <span style="color: #00a800;">2</span><span style="color: #d2cd86;">&gt;</span><span style="color: #d2cd86;">&amp;</span><span style="color: #00a800;">1</span>
cscript.exe %windir%<span style="color: #d2cd86;">\</span>system32<span style="color: #d2cd86;">\</span>slmgr.vbs <span style="color: #d2cd86;">/</span>ckms <span style="color: #d2cd86;">&gt;</span><span style="color: #e66170; font-weight: bold;">nul</span> <span style="color: #00a800;">2</span><span style="color: #d2cd86;">&gt;</span><span style="color: #d2cd86;">&amp;</span><span style="color: #00a800;">1</span>
cscript.exe %windir%<span style="color: #d2cd86;">\</span>system32<span style="color: #d2cd86;">\</span>slmgr.vbs <span style="color: #d2cd86;">/</span>cpky <span style="color: #d2cd86;">&gt;</span><span style="color: #e66170; font-weight: bold;">nul</span> <span style="color: #00a800;">2</span><span style="color: #d2cd86;">&gt;</span><span style="color: #d2cd86;">&amp;</span><span style="color: #00a800;">1</span>
cscript.exe %windir%<span style="color: #d2cd86;">\</span>system32<span style="color: #d2cd86;">\</span>slmgr.vbs <span style="color: #d2cd86;">/</span>ipk 93MGM-NTFKD-6BK63-R6FYR-6Q9PB
</pre>
