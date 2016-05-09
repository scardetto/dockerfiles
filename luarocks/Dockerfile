FROM scardetto/openresty

ENV LUAROCKS_VERSION 2.3.0
ENV LUAJIT_PREFIX /opt/openresty/luajit

# Install LuaRocks
RUN mkdir -p /tmp/luarocks \
  && cd /tmp/luarocks \
  && echo "==> Installing dependencies..." \
  && apk --no-cache add unzip curl openssl-dev make g++ gcc \
  && echo "==> Downloading LuaRocks..." \
  && curl -sSL http://luarocks.org/releases/luarocks-${LUAROCKS_VERSION}.tar.gz | tar -xvz \
  && cd luarocks-$LUAROCKS_VERSION/ \
  && echo "==> Installing LuaRocks..." \
  && ./configure \
    --prefix=$LUAJIT_PREFIX \
    --with-lua=$LUAJIT_PREFIX \
    --with-lua-include=$LUAJIT_PREFIX/include/luajit-2.1 \
  && make \
  && make install \
  && echo "==> Finishing..." \
  && rm -rf /tmp/luarocks \
  && ln -sf ${LUAJIT_PREFIX}/bin/luarocks /usr/local/bin/luarocks
