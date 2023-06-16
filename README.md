<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

Huwa rakkomandat li tinstalla nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) l-ewwel, u mbagħad `direnv allow` wara li tidħol fid-direttorju ( [il-.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) se jiġi eżegwit awtomatikament wara li jidħol fid-direttorju).

It-tifsira hija: traduzzjoni Ċiniża għall-Ġappuniż, Korean, Ingliż, traduzzjoni bl-Ingliż għal-lingwi l-oħra kollha. Jekk trid tappoġġja biss iċ-Ċiniż u l-Ingliż, tista 'biss tikteb `zh: en` .

It-tifsira hija: traduzzjoni Ċiniża għall-Ġappuniż, Korean, Ingliż, traduzzjoni bl-Ingliż għal-lingwi l-oħra kollha. Jekk trid tappoġġja biss iċ-Ċiniż u l-Ingliż, tista 'biss tikteb `zh: en` .

* [kodiċi front-end](https://github.com/xxai-art/web)
* [Pakketti tal-lingwa għas-sit kollu kemm hu](https://github.com/xxai-art/web/tree/main/i18n)
* [Pakketti tal-lingwa għall-moduli tal-login](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Websajt Dokumentazzjoni Multilingwi](https://github.com/xxai-doc)

Il-lingwa ta' programmar front-end hija [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , li żżid xi karatteristiċi bbażati fuq is-sintassi tal-coffeescript, ara [./coffee_plus.md](./coffee_plus.md) .

## Internazzjonalizzazzjoni ta' websajts u dokumenti

Ibni fuq it-3 proġetti li ġejjin

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  Is-suffiss huwa `.mdt` , tista' tuża s-sintassi simili għal `<+ ./coffee_plus/import.js>` biex tirreferi għal fajls esterni, u tiġġenera markdown bis-suffiss `.md` .

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  It-traduzzjoni ta' Markdown mhux se tittraduċi kodiċijiet u links, u se tpoġġi sentenzi tradotti fil-cache. Jekk it-traduzzjoni tiġi modifikata iżda t-test oriġinali ma jiġix modifikat, l-eżekuzzjoni tagħha mill-ġdid ma tissostitwixxix il-modifika tat-traduzzjoni.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  Fajls tal-lingwa għat-traduzzjoni ta' websajts iġġenerati minn `yaml` .

### Istruzzjonijiet għall-Awtomazzjoni tat-Traduzzjoni tad-Dokumenti

Ara r-repożitorju tal-kodiċi [xxai-art/doc](https://github.com/xxai-art/doc)

Huwa rakkomandat li tinstalla nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) l-ewwel, u mbagħad `direnv allow` wara li tidħol fid-direttorju ( [il-.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) se jiġi eżegwit awtomatikament wara li jidħol fid-direttorju).

Sabiex nevita l-bażi ta 'kodiċi kbira tradotta f'mijiet ta' lingwi, ħloqt bażi ta 'kodiċi separata għal kull lingwa u ħloqt organizzazzjoni biex taħżen il-bażi ta' kodiċi

L-issettjar tal-varjabbli ambjentali `GITHUB_ACCESS_TOKEN` u mbagħad it-tħaddim [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) awtomatikament joħloq ir-repożitorju tal-kodiċi.

Naturalment, tista 'wkoll tpoġġiha f'bażi ​​ta' kodiċi.

Referenza tal-iskrittura tat-traduzzjoni [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Il-kodiċi tal-iskript huwa interpretat kif ġej:

[bunx](https://bun.sh/docs/cli/bunx) huwa sostitut għal npx, li huwa aktar mgħaġġel. Naturalment, jekk ma jkollokx bun installat, tista 'tuża `npx` minflok.

`bunx mdt zh` jirrendi `.mdt` fid-direttorju zh bħala `.md` , ara ż-2 fajls marbuta hawn taħt

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` huwa l-kodiċi ewlieni għat-traduzzjoni (jekk għandek installati biss `nodejs` , iżda `bun` u `direnv` mhumiex installati, tista 'wkoll tħaddem `npx i18n` biex tittraduċi).

Se parse [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) , il-konfigurazzjoni ta ' `i18n.yml` f'dan id-dokument hija kif ġej:

```
en:
zh: ja ko en
```

It-tifsira hija: traduzzjoni Ċiniża għall-Ġappuniż, Korean, Ingliż, traduzzjoni bl-Ingliż għal-lingwi l-oħra kollha. Jekk trid tappoġġja biss iċ-Ċiniż u l-Ingliż, tista 'biss tikteb `zh: en` .

L-aħħar huwa [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , li jiġbed il-kontenut bejn it-titolu prinċipali u l-ewwel sottotitolu ta `README.md` ta’ kull lingwa biex jiġġenera dħul `README.md` . Il-kodiċi huwa sempliċi ħafna, tista 'tħares lejha lilek innifsek.

Google API jintuża għat-traduzzjoni b'xejn. Jekk ma tistax taċċessa Google, jekk jogħġbok ikkonfigura u waqqaf proxy, bħal:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

L-iskrittura tat-traduzzjoni se tiġġenera cache tradotta fid-direttorju `.i18n` , jekk jogħġbok iċċekkjaha bl- `git status` u żidha mar-repożitorju tal-kodiċi biex tevita traduzzjonijiet ripetuti.

Jekk jogħġbok mexxi `bunx i18n` kull darba li timmodifika t-traduzzjoni biex taġġorna l-cache.

Jekk it-test oriġinali u t-traduzzjoni huma modifikati fl-istess ħin, il-cache se jkun konfuż, għalhekk jekk trid timmodifika, tista 'timmodifika waħda biss, u mbagħad tħaddem `bunx i18n` biex taġġorna l-cache.
