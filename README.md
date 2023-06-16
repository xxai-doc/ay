<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

Mä chiqax código sitio web ukax código abierto ukawa, jaqukipäw sum yanapt’añatakix wali askiwa.

## nayraqata uñtawi

* [nayraqata uñtawi](https://github.com/xxai-art/web)
* [Taqi sitio ukatakix aru paquetes ukanakaw utji](https://github.com/xxai-art/web/tree/main/i18n)
* [Aru paquetes ukax módulos de ingreso ukanakatakiw utji](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Sitio Web Walja Arut Qillqatanaka](https://github.com/xxai-doc)

Front-end programación aruxa [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , ukax mä qawqha lurawinakampiw yapxati coffeescript sintaxis ukarjam, [./coffee_plus.md](./coffee_plus.md) uñakipt’aña.

## Internacionalización de sitios web ukat documentos ukanaka

Aka 3 lurawinakampiw lurasi

* [@w5/mdt ukat juk’ampinaka](https://www.npmjs.com/package/@w5/mdt)

  Sufijo ukax `.mdt` , `<+ ./coffee_plus/import.js>` ukar uñtasit sintaxis ukampiw anqäx qillqatanakar uñt’ayañatakix apnaqasispa, ukatx `.md` sufijo ukampiw markdown uñstayasispa.

* [@w5/trmd ukat juk’ampinaka](https://www.npmjs.com/package/@w5/trmd)

  Markdown jaqukipäwix janiw códigos ukat enlaces ukanakar jaqukipkaniti, ukatx jaqukipat aruchjanakax caché ukanw jaqukipatäni. Jaqukipäwix mayjt’ayatächi ukampis nayrïr qillqatax jan mayjt’ayatäkchi ukhaxa, wasitat phuqhañax janiw jaqukipäwin mayjt’äwipxa chhaqtayatäkaniti.

* [@w5/i18n ukat juk’ampinaka](https://www.npmjs.com/package/@w5/i18n)

  `yaml` ukan lurat sitios web ukar jaqukipañatakix arut arsuwinakaw utji.

### Documento Jaqukipaña Automatización ukan yatichäwipa

Uñxatt’añataki imañ uta [xxai-art/doc](https://github.com/xxai-art/doc)

Nayraqatax nodejs, [direnv](https://direnv.net) ukat [bun ukanakaw](https://github.com/oven-sh/bun) utt’ayañax wakisi, ukatx directorio ukar mantañ tukuyatat `direnv allow` apnaqañaw wakisi.

Patak patak arunakar jaqukipat sinti jach’a almacenes ukanakar jan puriñapatakix sapa arut mä sapa almacén de código ukham lurawayta ukatx mä tamaw aka almacén ukar imañatak lurawayta

Pachamaman variable `GITHUB_ACCESS_TOKEN` utt’ayaña ukat [create.github.coffee ukar](https://github.com/xxai-art/doc/blob/main/create.github.coffee) apnaqañax automáticamente almacén uñstayañapawa.

Chiqansa, mä almacén ukar ucharaksnawa.

Jaqukipaña script referencia [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Uka script code ukax akham qhanañchatawa:

[bunx](https://bun.sh/docs/cli/bunx) ukax npx ukat lantintatawa, ukax juk’amp jank’akiw. Chiqans, jan bun ukan utjki ukhax `npx` uka lantiw apnaqasispa.

`bunx mdt zh` ukax `.mdt` ukarux zh directorio ukanx `.md` ukham uñacht’ayi, 2 uñakipt’at qillqatanakax akham uñakipt’atawa

* [café_plus.mdt ukax mä juk’a pachanakanwa](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [café_plus.md ukat juk’ampinaka](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` ukax jaqukipañatakix código central ukawa ( `nodejs` ukakiw utji, ukampis `bun` ukat `direnv` janiw instalatäkiti, ukatx `npx i18n` ukax jaqukipañatakiw apnaqasispa).

Ukax [i18n.yml ukar](https://github.com/xxai-art/doc/blob/main/i18n.yml) uñakipañapawa, aka qillqatanx `i18n.yml` ukan configuración ukax akhamawa:

```
en:
zh: ja ko en
```

Ukax akham sañ muni: chino arut jaqukipata japonés, coreano, inglés, inglés arut taqpach yaqha arunakar jaqukipata. Chino ukat inglés arunakaruki yanapt’añ munsta ukhax `zh: en` qillqt’asma.

Qhipïrix [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , ukax sapa arun `README.md` ukan jach’a sutimp nayrïr subtítulo ukamp taypin utjki ukanak apsu, mä qillqt’äw `README.md` uñstayañataki. Código ukax wali ch’amawa, juma pachpaw uñakipt’asma.

Google API ukax inaki jaqukipañatakiw apnaqasi. Google ukar jan mantañax utjkchi ukhax mä proxy ukar uñt’ayañamawa ukat uñt’ayañamawa, sañäni:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Jaqukipañ qillqatax mä jaqukipäw caché `.i18n` directorio ukan lurani, `git status` ukamp uñakipt’aña ukat código imañ utar yapxataña jan walja kuti jaqukipañataki.
