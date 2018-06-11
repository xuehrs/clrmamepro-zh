#本工具是基于aur的clrmamepro脚本修改而成的，主要特点就是支持中文、缺点就是基于wine平台。
#恩恩，他只是mame街机游戏rom管理工具。cmp4034_64-cht.tar.gz这个包是基于cmp4034_64-cht.7z打包的，未做任何修改，请放心使用
#bug联系736363980@qq.com 或者 github.com/xuehrs/clrmamepro-zh


pkgname=clrmamepro-cn-zh
pkgver=4.034
pkgrel=1
pkgdesc="这是一个中文版clrmamepro，基于wine运行"
arch=('any')
url="http://f.ppxclub.com/686177-1-1"
license=('custom')
depends=('wine'
	  'wqy-microhei')
makedepends=('icoutils')
source=("https://raw.githubusercontent.com/xuehrs/clrmamepro-zh/master/cmp4034_64-cht.tar.gz"
        "clrmamepro-zh"
        "clrmamepro-zh.desktop"
	 "wqy-microhei.reg")
sha256sums=('SKIP'
            'SKIP'
            'SKIP'
	     'SKIP')

build() {
  cd cmp4034_64-cht/
  wrestool -x -n 500 -o . cmpro64.exe
  icotool -x -o . cmpro64.exe_14_500_1031.ico
}

package() {
  #解决中文字体乱码问题
  install -Dm644 "${srcdir}/wqy-microhei.reg" "${pkgdir}/usr/share/clrmamepro-zh/wqy-microhei.reg"

  install -Dm644 "${srcdir}/cmp4034_64-cht/7z_64.dll" "${pkgdir}/usr/share/clrmamepro-zh/7z_64.dll"
  install -Dm755 "${srcdir}/cmp4034_64-cht/cmpro64.exe" "${pkgdir}/usr/share/clrmamepro-zh/cmpro64.exe"
  install -Dm644 "${srcdir}/cmp4034_64-cht/engine.cfg" "${pkgdir}/usr/share/clrmamepro-zh/engine.cfg"
  install -Dm644 "${srcdir}/cmp4034_64-cht/setformat.xml" "${pkgdir}/usr/share/clrmamepro-zh/setformat.xml"
  install -Dm644 "${srcdir}/cmp4034_64-cht/stats.ini" "${pkgdir}/usr/share/clrmamepro-zh/stats.ini"
  install -Dm644 "${srcdir}/cmp4034_64-cht/unrar64.dll" "${pkgdir}/usr/share/clrmamepro-zh/unrar64.dll"
  install -Dm644 "${srcdir}/cmp4034_64-cht/update.dll" "${pkgdir}/usr/share/clrmamepro-zh/update.dll"
  install -Dm644 "${srcdir}/cmp4034_64-cht/urls.ini" "${pkgdir}/usr/share/clrmamepro-zh/urls.ini"
  install -Dm644 "${srcdir}/cmp4034_64-cht/version64.ini" "${pkgdir}/usr/share/clrmamepro-zh/version64.ini"

  install -Dm755 "${srcdir}/clrmamepro-zh" "${pkgdir}/usr/bin/clrmamepro-zh"

  install -Dm644 "${srcdir}/clrmamepro-zh.desktop" "${pkgdir}/usr/share/applications/clrmamepro-zh.desktop"

  install -Dm644 "${srcdir}/cmp4034_64-cht/cmpro64.exe_14_500_1031_4_16x16x32.png" "${pkgdir}/usr/share/icons/hicolor/16x16/apps/clrmamepro-zh.png"
  install -Dm644 "${srcdir}/cmp4034_64-cht/cmpro64.exe_14_500_1031_5_32x32x32.png" "${pkgdir}/usr/share/icons/hicolor/32x32/apps/clrmamepro-zh.png"
  install -Dm644 "${srcdir}/cmp4034_64-cht/cmpro64.exe_14_500_1031_6_48x48x32.png" "${pkgdir}/usr/share/icons/hicolor/48x48/apps/clrmamepro-zh.png"
}


