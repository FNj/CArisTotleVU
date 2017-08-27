# Adaptivní testování
Adaptivní počítačové testování je způsob testování, při kterém se průběh testu mění na základě informací získaných v průběhu testu. V anglicky psané literatuře se pro toto používá označení computerized adaptive testing (CAT). Možným přínosem adaptivního testování je zvýšení přesnosti měření dovedností a úspora času.



# Bayesovské sítě

Pro výběr otázek v rámci našeho přístupu k adaptivnímu testování se používá bayesovských sítí. Jedná se o grafický model (ve smyslu teorie grafů) popisující vztahy mezi náhodnými veličinami pomocí podmíněných pravděpodobnostních rozdělení. Formálně lze bayesovskou síť definovat následujícím způsobem.

## Formální definice
Nechť je $V$ množina náhodných veličin. Pak je bayesovská síť nad $V$ uspořádaná dvojice $(B_S,B_P)$, kde $B_S$ je orientovaný acyklický graf s uzly $V$ (tzv. struktura sítě) a $B_P$ je množina funkcí $p$ -- jedna pro každou $v \in V$ -- , které udávají podmíněné pravděpodobnostní rozdělení $v$ v závislosti na hodnotě (přímých) předchůdců $v$ v $B_S$.

V našem případě budou $v$ nabývat jen určitých diskrétních hodnot, takže si prvky $B_P$ můžeme také představovat prostě jako funkce zobrazující vektor stavů předchůdců $v$ v $B_S$ na vektor pravděpodobností stavů $v$. Prakticky lze takového funkce zapsat jako tabulku.

## Neformální popis
Bayesovské sítě vlastně popisují statisticky získané a popsané kauzální vztahy mezi nějakými pozorovanými událostmi. V našem případě půjde kauzální vztah mezi odpověďmi studenta na otázky v testu a jeho měřenými dovednostmi.

Jeden z předpokladů pro běžné výpočty v bayesovských sítích je, že pro každou veličinu z $V$ platí, že je podmíněně nezávislá na veličinách, které **ne**jsou reprezentovány jejími potomky v síti, při znalosti stavu veličin reprezentovaných jejími předky v síti. Zkráceně: každá veličina je podmíněně nezávislá na svých nepotomcích při znalosti svých předků.

## Příklady
V [x](almond_tlustospis) je hned v úvodu jako příklad uvedena síť na obrázku [x] 

Jako příklad lze také použít přímo jednu ze sítí, která se používala přímo pro účely adaptivního testování. Na grafu [x][příklad sítě 2] zelené uzly reprezentují jednotlivé dovednosti a žluté uzly otázky. Uzel *S8* (celková dovednost, např. znalost středoškolské matematiky) tvoří v podstatě kořen celého grafu (byť se nejedná o strom), následují ostatní zelené uzly (jednotlivé prvky celkové dovednosti, např. znalost geometrie, algebry apod.) a na konec žluté uzly, které reprezentují jednotlivé otázky v testu.

# Životní cyklus adaptivního testu





[notace grafů]: https://is.mendelu.cz/eknihovna/opory/zobraz_cast.pl?cast=9295 (Notace pojmů z teorie grafů)
[příklad sítě 2]: complex_BN_plajner16.pdf (Příklad bayesovské sítě pro adaptivní testování z článku Student Skill Models in Adaptive Testing, Plajner & Vomlel)
