@@ -0,0 +1,20 @@
Se habilitó la nueva transmisión del canal 1                                                       
configurar canal1 entrada https://streaming-cl.sh1ny.space/memfs/4f2393d1-64eb-4e8f-a2f4-f60feea9e63d.m3u8                                        
configurar salida del canal 1 #duplicate{dst=mosaic-bridge{id=1,height=144,width=180},select=video,dst=bridge-out{id=1},select=audio}                                                         
                                                                                
Se habilitó la nueva transmisión del canal 2
configurar canal2 entrada https://stream.wifiexpert.cl/kanade/kanadetv/playlist.m3u8
configurar salida del canal 2 #duplicate{dst=mosaic-bridge{id=2,height=144,width=180},select=video,dst=bridge-out{id=2},select=audio}                                                         
Se habilitó la nueva transmisión del canal 3
configurar canal3 entrada https://mitv.zplay.cl/Bakup/index.m3u8
configurar salida del canal 3 #duplicate{dst=mosaic-bridge{id=3,height=144,width=180},select=video,dst=bridge-out{id=3},select=audio}                                                         
Nueva transmisión en segundo plano habilitada
configurar entrada de fondo /ruta/completa/al/fondo.png
configurar salida en segundo plano #transcode{sfilter=mosaic,vcodec=mp2v,vb=10000,scale=1}:bridge-in{delay=400,id-offset=100}:standard{access=udp,mux=ts,url=239.255.12.42,sap,name="mosaic"}
controlar la reproducción en segundo plano
control de reproducción del canal 1
control de reproducción del canal 2
Controlar la reproducción del canal 3
0 commit comments
Comments
0
 (0)