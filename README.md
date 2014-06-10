cups4android
============
### configure ###

        cd $(SOURCE_DIR); PKG_CONFIG_PATH=$(PKG_CONFIG_PATH) ./configure \
          --host=$(HOST) --prefix=$(DEST_DIR) --with-optim="-Wall -Wno-format-y2k \
          -Wunused -fPIC -Os -g" --disable-gssapi ac_cv_func_strtoll="yes" \
          ac_cv_search_abs="none required"

### build ###

        cd $(SOURCE_DIR)/cups; make
        cd $(SOURCE_DIR)/berkeley; make

### install ###

        cd $(SOURCE_DIR)/cups; make install
        cd $(SOURCE_DIR)/berkeley; make install
