<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

Parti mill-kodiċi tal-websajt hija sors miftuħ, merħba biex tgħin tottimizza t-traduzzjoni.

## kodiċi front-end

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
