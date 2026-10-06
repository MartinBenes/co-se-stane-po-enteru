# Co se stane po Enteru

Interaktivní prezentace pro první seminář o správě sítí. Dvanáct snímků, plán na 65 minut, průběžné otázky a společná detektivka nad sítí učebny.

**Spustit:** [prezentace](https://benes.dev/co-se-stane-po-enteru/)

## Ovládání

- Šipky vlevo a vpravo, mezerník nebo tlačítka dole přepínají snímky.
- `N` zapíná poznámky pro vyučujícího, včetně vysvětlení a zdrojů.
- `F` zapíná celou obrazovku.
- Horní lišta obsahuje stopky hodiny, jednotlivé úlohy mají vlastní časovač.
- Příkazy se přepínají pro Windows, Linux a macOS.
- Síťová mapa přijímá masku v desetinném tvaru, prefix `/24` i hexadecimální masku z macOS.

Prezentace je v jediném souboru `index.html`. Lze ho otevřít přímo v prohlížeči. Webová písma se načítají z Google Fonts, bez připojení se použijí systémová písma. Hodnoty zadané do mapy se zpracovávají pouze v prohlížeči.

## Výukové zjednodušení

Příběh na snímku 10 jde od připojení k síti po načtení webu. DHCP tedy probíhá před stiskem Enter. Příklad předpokládá IPv4, HTTPS přes TCP a DNS mimo místní podsíť. ARP je potřeba, pokud už nemáme MAC dalšího uzlu v cache. Směrování doprovází všechny IP pakety, včetně DNS. HTTP/3 používá QUIC přes UDP, což připomíná snímek 11.

Diagnostika nabízí další postup podle výsledků testů. Neúspěšný ping sám neurčuje místo výpadku. Názvy hopů ani první veřejná IP v traceroute spolehlivě neurčují hranici fakulty. `pedf.cuni.cz` může být dostupný uvnitř sítě UK bez cesty přes CESNET.

V poznámkách ke snímku 6 jsou také upřesnění dodaného klíče: neautoritativní DNS odpověď nemusí pocházet z cache a náhodná MAC adresa neumožňuje běžné určení výrobce podle OUI.

Organizační údaje, podmínky zápočtu a plán setkání vycházejí z dodaného materiálu.

## Zdroje

- [RFC 2131: DHCP](https://www.rfc-editor.org/rfc/rfc2131.html)
- [RFC 826: ARP](https://www.rfc-editor.org/rfc/rfc826.html)
- [RFC 1034: DNS a cache](https://www.rfc-editor.org/rfc/rfc1034.html) a [RFC 1035: autoritativní odpověď](https://www.rfc-editor.org/rfc/rfc1035.html#section-4.1.1)
- [RFC 1918: privátní adresy](https://www.rfc-editor.org/rfc/rfc1918.html) a [IANA: zvláštní IPv4 rozsahy](https://www.iana.org/assignments/iana-ipv4-special-registry/iana-ipv4-special-registry.xhtml)
- [RFC 3927: IPv4 link-local](https://www.rfc-editor.org/rfc/rfc3927.html) a [RFC 3021: prefix /31](https://www.rfc-editor.org/rfc/rfc3021.html)
- [RFC 9293: TCP](https://www.rfc-editor.org/rfc/rfc9293.html), [RFC 8446: TLS](https://www.rfc-editor.org/rfc/rfc8446.html) a [RFC 9114: HTTP/3](https://www.rfc-editor.org/rfc/rfc9114.html)
- [Microsoft: ping](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/ping) a [tracert](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/tracert)
- [Apple: výběr síťového rozhraní](https://developer.apple.com/documentation/network/recording-a-packet-trace) a [náhodné MAC adresy](https://support.apple.com/guide/security/sec31e483abf/web)
- [IEEE: OUI](https://standards.ieee.org/products-programs/regauth/oui/)
- [Cloudflare: resolver 1.1.1.1](https://developers.cloudflare.com/1.1.1.1/)
- [CESNET](https://www.cesnet.cz/)
- [Kurose a Ross: materiály autorů, kapitola 1](https://gaia.cs.umass.edu/kurose_ross/videos/1/)

## GitHub Pages

Publikování z větve `main`, kořen repozitáře. Soubor `.nojekyll` vypíná zpracování Jekyllem. Pro další úpravu stačí změnit `index.html` a nahrát commit do `main`.
