pkgname=cachyos-hello-concept
pkgver=0.3.0
pkgrel=1
pkgdesc="A modern Qt6/QML UI/UX concept mockup for CachyOS Hello"
arch=('any')
url="https://github.com/AwwsmGaurav/cachyos-hello-concept"
license=('MIT')
depends=('python' 'pyside6' 'noto-fonts')
source=()

package() {
    install -dm755 "$pkgdir/usr/share/$pkgname"
    cp -r "$startdir/main.py" "$startdir/ui" "$startdir/data" "$startdir/assets" "$pkgdir/usr/share/$pkgname/"

    install -dm755 "$pkgdir/usr/bin"
    cat << 'EOF' > "$pkgdir/usr/bin/$pkgname"
#!/bin/sh
exec python /usr/share/cachyos-hello-concept/main.py "$@"
EOF
    chmod 755 "$pkgdir/usr/bin/$pkgname"
}