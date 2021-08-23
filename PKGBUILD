# Maintainer: Zarren Spry (drgr33n) <zarrenspry@gmail.com>

pkgname=teams-chromium
pkgver=0.1
pkgrel=1
pkgdesc="Microsoft Teams for Linux is your chat-centered workspace in Office 365"
arch=('any')
url="https://teams.microsoft.com"
license=('GPL-3.0')
depends=("chromium")
optdepends=("xdg-desktop-portal: Screen sharing support"
            "xdg-desktop-portal-gtk: Screen sharing support for Gnome"
            "xdg-desktop-portal-kde: Screen sharing support for KDE"
            "xdg-desktop-portal-wlr: Screen sharing support for Sway DWL")

package() {
  # install launcher
  install -dm755 "${pkgdir}/usr/share/applications/"
  install -dm755 "${pkgdir}/usr/share/pixmaps/"
  cp "${srcdir}/usr/share/applications/microsoft-teams-chrome.desktop" "${pkgdir}/usr/share/applications/microsoft-teams-chrome.desktop"
  cp "${srcdir}/usr/share/pixmaps/teams.png" "${pkgdir}/usr/share/pixmaps/teams.png"

  # Move license
  install -dm755 "${pkgdir}/usr/share/licenses/${pkgname}"
  cp "${srcdir}/../LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}"
}
