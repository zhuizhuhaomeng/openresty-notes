# enable debug log
./configure -j2 --with-pcre=pcre-8.00 --with-http_realip_module --with-stream_realip_module --with-debug

# enable dd debug
## enable all dd debug
./configure -j2 --with-pcre=pcre-8.00 --with-http_realip_module --with-stream_realip_module --with-debug --with-cc-opt="-D DDEBUG=1"

## enabe dd debug for one module
1. add "#define DDDEBUG 1" to bundle/ngx_lua-0.10.16rc5/src/ddebug.h
2. ./configure -j2 --with-pcre=pcre-8.00 --with-http_realip_module --with-stream_realip_module --with-debug 
