<script>
import SQLiteService from '@/services/SQLiteService.js'
import { useFindSummaries, useFindCollapsible, usePopUp} from "@/assets/javascript/revealText.js"
import { useRevealMedia } from "@/assets/javascript/revealMedia.js"
import { useShare} from "@/assets/javascript/share.js"


export default {
   methods:{
    async addNote(noteid){
       var noteText = document.getElementById(noteid).value
       var noteHeight = await SQLiteService.addNote(noteid, this.$route.name, noteText)
       document.getElementById(noteid).style.height = noteHeight
    },
    goToPageAndSetReturn(gotoPath){
      localStorage.setItem("returnpage", this.$route.name);
      this.$router.push({
        path: gotoPath,
      })
    },
    pageGoBack(returnto){
      if (localStorage.getItem("returnpage")) {
        returnto = localStorage.getItem("returnpage");
        localStorage.removeItem("returnpage")
      }
      this.$router.push({
        name: returnto,
      })
    },
    popUp(verse){
      usePopUp(verse)
    },
    share(what, v1, v2){
      useShare(what, v1, v2)
    },
    vuePush(id){
      this.$router.push({
        name: id,
      })
    },
  },
  async mounted() {
    localStorage.setItem("lastpage", this.$route.name)
    useFindSummaries()
    useFindCollapsible()
    useRevealMedia()
    await SQLiteService.notes(this.$route.name)
  },
}
</script>
<template>
  <div id="nav">
    <div class="nav full internal-link" @click="this.pageGoBack('fra-tc-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>2.</h1></div>
                        <div class="chapter_title ltr"><h1>L'amour et le pardon de Dieu</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <p><em>Il y avait de profondes rides sur le jeune visage qui fixait le dehors &agrave; travers la fen&ecirc;tre du train, des rides laiss&eacute;es par des mois pass&eacute;s &agrave; revivre des temps regrettable pendant qu&rsquo;il purgeait sa peine en prison. </em><br />
<br />
<em>Les collines verdoyantes et les p&acirc;turages familiers d&eacute;filaient jusqu&rsquo;&agrave; ce que l&agrave;, &agrave; l&rsquo;horizon, il reconnut les trois fl&egrave;ches du grenier de sa ville natale. Une boule de terreur monta soudain dans sa gorge et descendit le long de son estomac. Il le saurait bient&ocirc;t. Il n&rsquo;y avait que quelques kilom&egrave;tres qui le s&eacute;paraient de la&nbsp; demeure de ses parents situ&eacute;e &agrave; la p&eacute;riph&eacute;rie de&nbsp; la ville. </em><br />
<br />
<em>Il caressa&nbsp; la couverture du livre qui &eacute;tait rest&eacute; ouvert sur ses genoux comme pour toucher quelque reste de r&eacute;alit&eacute;. Toutes ces choses paraissaient pour lui&nbsp; un r&ecirc;ve&nbsp;? Les trois derni&egrave;res ann&eacute;es ont &eacute;t&eacute; envelopp&eacute;es de brouillard. Comment avait-il pu le faire&nbsp;? La honte dont son&nbsp; crime a couvert sa m&egrave;re et son p&egrave;re &eacute;tait plus que ce que quiconque aurait &agrave; supporter. Comment pourraient-ils jamais lui&nbsp; pardonner&nbsp;?&nbsp; </em><br />
<br />
<em>Et pendant ce temps, le train roulait se rapprochant plus de ce qui avait &eacute;t&eacute; autrefois &hellip;un domicile pour lui. Il se rappelait quand il leur avait &eacute;crit disant qu&rsquo;il n&rsquo;avait aucun droit mais il avait demand&eacute; de laisser un signe si quelque part dans leur&nbsp; c&oelig;ur il se trouvait une place pour lui pardonner. Juste un ruban blanc accroch&eacute; au vieux ch&ecirc;ne de l&rsquo;arri&egrave;re-cour o&ugrave; se trouvait son pneu qui&nbsp; se balan&ccedil;ait toutes ces ann&eacute;es &eacute;tait tout ce dont il avait besoin.. Il voulait seulement les voir une fois de plus, ensuite il avait l&rsquo;intention de s&rsquo;en aller pour les &eacute;pargner de tout autre honte et blessure. Il le saurait dans les quelques minutes qui viennent.&nbsp; </em><br />
<br />
<em>Il avait les mains moites, sa bouche &eacute;tait s&egrave;che, et autant qu&rsquo;il d&eacute;sirait le savoir, il ne pouvait pas se permettre de regarder par la fen&ecirc;tre. Que ferait-il si le ruban n&rsquo;&eacute;tait pas l&agrave;&nbsp;? </em><br />
<br />
<em>&laquo;&nbsp;Tu vas bien, fiston&nbsp;?&nbsp;&raquo; Le passager qui &eacute;tait &agrave; c&ocirc;t&eacute;&nbsp;de lui ne pouvait pas s&rsquo;emp&ecirc;cher de remarquer le chagrin du jeune homme. &laquo;&nbsp;Il y a-t-il une chose que je peux faire pour toi&nbsp;?&nbsp;&raquo; &lsquo;&nbsp;&laquo;&nbsp;Oui Monsieur, il y en a&nbsp;&raquo;&nbsp;: dit-il. Juste apr&egrave;s ce tournant se trouve&nbsp; un grand ch&ecirc;ne et bien je sais que cela semble &ecirc;tre un peu &eacute;trange, mais pouvez vous me dire si vous voyez un ruban jaune quelque part dans l&rsquo;arbre&nbsp;? Je,&hellip; je ne parviens pas &agrave; me convaincre de regarder&nbsp;&raquo; </em><br />
<br />
<em>L&rsquo;homme hocha la t&ecirc;te et &agrave; mesure que le train virait au&nbsp; tournant, il commen&ccedil;a &agrave; sourire.&nbsp;&laquo;&nbsp;Est-ce que c&rsquo;est l&agrave;&nbsp;?&nbsp;&raquo; le jeune homme demanda&nbsp; &laquo;&nbsp;Pouvez-vous voir le ruban&nbsp;&raquo; </em><br />
<br />
<em>&laquo;&nbsp;Tu devras regarder par toi-m&ecirc;me, fiston&nbsp;&raquo; dit l&rsquo;homme &laquo;&nbsp;Tu ne me croirais pas si je te le disais&nbsp;&raquo; </em><br />
<br />
<em>Le jeune leva la t&ecirc;te humblement et regarda fixement avec un scepticisme sinc&egrave;re. Le ch&ecirc;ne avait fleuri des bouquets de rubans jaunes qui planaient sur chaque branche au gr&eacute; de la brise. Et contre le mur de la cl&ocirc;ture un homme et une femme&nbsp; faisaient signe de la main au train&nbsp; qui passait et &agrave; bord duquel se trouvait leur fils qu&rsquo;ils aimaient.</em><br />
<br />
Il y a des chr&eacute;tiens qui, comme ce jeune homme, m&egrave;nent une vie remplie de crainte, manquant cet &eacute;clat de lumi&egrave;re, cette dynamique exceptionnelle qu&rsquo;ils avaient esp&eacute;r&eacute; du Christianisme. Ils ne sourient pas.&mdash; Ils renfrognent la mine. Ils se d&eacute;battent. Ils sont accabl&eacute;s par les fardeaux. <em>O&ugrave; est la paix que J&eacute;sus a promise&nbsp;?</em>&nbsp;&nbsp; se demandent-ils. Ce dont ils ont r&eacute;ellement besoin c&rsquo;est une perspective renouvel&eacute;e du pardon qui est le n&ocirc;tre en Christ.<br />
<br />
Ces croyants se rendent comptent avec peine que quelque chose manquent leurs vie. Leur Christianisme refl&egrave;te une monotonie auto inflig&eacute;e. Ces personnes l&agrave; n&rsquo;ont pas besoin de r&eacute;primande de la part des fr&egrave;res et s&oelig;urs Chr&eacute;tiens bien intentionn&eacute;s. Ils n&rsquo;ont pas besoin d&rsquo;&ecirc;tre convaincus que la vie est vide de sens et peu &eacute;panouissante. Ce dont ils ont besoin en effet, est de puiser dans leurs ressources spirituelles. (e.g.,amour, paix et pardon)&mdash; ces ingr&eacute;dients manquant que leur salut peut apporter &agrave; leurs vies quotidiennes. C&rsquo;est leur l&eacute;gitime h&eacute;ritage, disponible pour tout croyant.<br />
<br />
Comme le jeune homme qui a vu les rubans jaunes, ces pauvres croyants ont simplement besoin de comprendre comment s&rsquo;y engager pour entrer en&nbsp; possession de ce qui est &agrave; eux et pour d&eacute;couvrir que le secret pour conna&icirc;tre et vivre le pardon&nbsp; r&eacute;side en le fait d&rsquo;&ecirc;tre rempli de l&rsquo;Esprit de Dieu.<br />
<br />
Mais que dirions-nous &agrave; celui-l&agrave; dont le Christianisme est terne&nbsp;? Et si vous &eacute;tiez en train de lutter pour retrouver l&rsquo;amour qui vous &eacute;chappe en tant que croyant&nbsp;? Serait-ce vraiment possible qu&rsquo;un autre Chr&eacute;tien vous pr&eacute;sente de profondes v&eacute;rit&eacute;s avec assez de clart&eacute; pour que vous en saisissiez le sens et les appliquiez &agrave; votre propre vie&nbsp;? Un croyant peut-il enseigner &agrave; un autre comment vivre l&rsquo;exp&eacute;rience du pardon&nbsp; infini du Christ par eux-m&ecirc;mes&nbsp;?<br />
<br />
La r&eacute;ponse est oui. Tout au long de notre marche avec Christ, nous trouvons des avantages satisfaisants dans la pratique de ce concept.<br />
<br />
Paul traite de ce sujet m&ecirc;me en 1Corinthiens 2 et3. Il explique la raison pour laquelle certains croyants manquent de joie et de la puissance du Saint-Esprit dans leur vie quand&nbsp; il &eacute;crit au sujet de l&rsquo;homme naturel, l&rsquo;homme spirituel et l&rsquo;homme&nbsp; charnel.</p>

<h2>L&rsquo;Homme Naturel</h2>

<p>L&rsquo;Homme Naturel est cet individu l&agrave; qui compte sur ses propres ressources. Cette personne dit&nbsp;: &laquo;&nbsp; Je le ferai comme bon me semble&nbsp;&raquo;. &laquo;&nbsp;Il n&rsquo;est pas un Chr&eacute;tien et donc ne peut pas saisir les v&eacute;rit&eacute;s de la Parole de Dieu. Il se suffit &agrave; lui-m&ecirc;me. Ses int&eacute;r&ecirc;ts et ses ambitions sont mondains et &eacute;gocentriques.&nbsp;&nbsp; Bien qu&rsquo;il semble y avoir une harmonie dans ses actes, il est spirituellement mort. (La mort est notre seul droit de naissance&nbsp; jusqu&rsquo;&agrave; ce que nous invitions J&eacute;sus dans nos vies.)</p>

<h2>L&rsquo;Homme Spirituelle</h2>

<p>L&rsquo;Homme Spirituelle est cet individu l&agrave; qui est n&eacute; de nouveau dans la vie &eacute;ternelle. Cette personne a conscience que, Je ne peux pas le faire par moi-m&ecirc;me, Je reconnais que j&rsquo;ai besoin de Dieu. Il est habit&eacute; et dirig&eacute; par l&rsquo;Esprit-Saint qui le rend capable de comprendre les v&eacute;rit&eacute;s qu&rsquo;enseigne la Parole de Dieu. L&rsquo;homme spirituel est vivant&nbsp;! Il a une relation vitale avec le Seigneur. Et parce qu&rsquo;il est un canal de la puissance de l&rsquo;Esprit Saint, il porte constamment du fruit.</p>

<h2>L&rsquo;Homme Charnel</h2>

<p>Le th&egrave;me principal&nbsp; de ce chapitre&nbsp; est l&rsquo;Homme&nbsp; Charnel. Bien qu&rsquo;il soit n&eacute; de nouveau, il n&rsquo;a pas encore&nbsp; puis&eacute; dans l&rsquo;abondant h&eacute;ritage de son P&egrave;re c&eacute;leste. Au contraire, il continue de vivre comme un homme condamn&eacute;. Il apparait souvent comme si tout va bien. Il peut enseigner &agrave; l&rsquo;Ecole de Dimanche, servir comme pasteur &agrave; l&rsquo;&eacute;glise ou consacrer des ann&eacute;es de sa vie sur un champ missionnaire au loin conduisant les autres &agrave; Christ. Mais c&rsquo;est du camouflage.<br />
<br />
L&rsquo;ultime v&eacute;rit&eacute; est qu&rsquo;un homme charnel vit une vie de d&eacute;faite. S&rsquo;il est honn&ecirc;te, il avouera que son Christianisme manque d&rsquo;une joie v&eacute;ritable. Il est constamment frustr&eacute;.&nbsp; Avec d&eacute;sespoir, il essaye courageusement de mener une vie&nbsp; qui plait &agrave; Dieu, mais au lieu de puiser &agrave; la source de la puissance, le Saint-Esprit, il s&rsquo;appuie sur sa propre &eacute;nergie et sa cr&eacute;ativit&eacute; pour la force dont il a besoin, et il se retrouve dans des probl&egrave;mes.<br />
<br />
(Il y a) autres choses qui caract&eacute;risent le style de vie de l&rsquo;homme charnel. Il peut s&rsquo;efforcer de s&rsquo;accrocher fermement &agrave; Dieu et refuser simultan&eacute;ment de lib&eacute;rer les choses mat&eacute;rielles, terrestres. Il se voit poss&eacute;der par ses possessions. Au m&ecirc;me moment, il essaye de vaquer aux choses spirituelles.<br />
<br />
J&eacute;sus Lui-m&ecirc;me a dit qu&rsquo;il est impossible de servir deux ma&icirc;tres. Bien que l&rsquo;homme charnel s&rsquo;efforce sinc&egrave;rement de plaire &agrave; Dieu, il ne fait aucun progr&egrave;s spirituel.&nbsp; Il est au commande de sa vie spirituelle. Romains8:7 en donne la raison: &laquo;&nbsp;car l&rsquo;affection de la chair est inimiti&eacute; contre Dieu, parce qu&rsquo;elle ne se soumet pas &agrave; la loi de Dieu, et qu&rsquo;elle ne le peut m&ecirc;me pas. &raquo; (LSG).<br />
<br />
Cette v&eacute;rit&eacute; renferme une immense libert&eacute;&nbsp;: <strong>C&rsquo;est notre foi en Dieu qui Lui plait,&nbsp; et non nos efforts, en d&eacute;pit de nos essais courageux ou de notre profonde sinc&eacute;rit&eacute;.</strong>&nbsp; Notre&nbsp; seul espoir&nbsp; pour&nbsp; la victoire&nbsp; sur cette tendance charnelle, est de faire confiance &agrave; Christ pour vivre Sa vie de r&eacute;surrection en nous et &agrave; travers nous. Son pardon devient n&ocirc;tre&nbsp; quand nous devenons Ses enfants. Nous avons seulement besoin&nbsp; de l&rsquo;accepter &ndash;un fait que l&rsquo;Homme Charnel ne comprend pas.<br />
<br />
L&rsquo;Homme Charnel peut ne pas s&rsquo;accrocher &agrave; sa propre force simplement&nbsp; par&nbsp; choix. Il est possible qu&rsquo;il souffre d&rsquo;un manque d&rsquo;informations fiable, ou il peut &ecirc;tre confus au sujet de qui Dieu&nbsp; est r&eacute;ellement&nbsp; et de ce que Dieu peut faire dans la vie d&rsquo;une personne.<br />
<br />
Imaginez&nbsp; l&rsquo;histoire d&rsquo;un pauvre immigrant qui un jour avait pay&eacute; sa travers&eacute;e sur un navire en destination des Etats-Unis. Il&nbsp; lui restait juste assez d&rsquo;argent pour quelques biscuits et quelque bloc de fromage qu&rsquo;il a pris soin de rationner sur les quelques premiers jours du voyage. Mais sa faim s&rsquo;&eacute;tait intensifi&eacute;e. Il regardait les serveurs du navire le d&eacute;passer avec empressement apportant des plateaux de fruits et de l&eacute;gumes succulents, de viande de poulets gras et des teaks juteux aux autres passagers.&nbsp; Finalement sa peur &eacute;tait subjugu&eacute;e par la senteur et il arr&ecirc;ta un serveur.<br />
<br />
&laquo;&nbsp;S&rsquo;il vous plait&nbsp;&raquo; dit-il en suppliant l&rsquo;homme qui &eacute;tait surpris. &laquo;Je suis affaibli par la faim&nbsp;&raquo;. Je ferai n&rsquo;importe quoi pour&nbsp; m&rsquo;offrir&nbsp; un&nbsp; repas&mdash; nettoyer&nbsp; les chambres, laver les ponts,&nbsp; faire la vaisselle&hellip;&nbsp;&raquo;<br />
<br />
&laquo;&nbsp;Voyagez-vous clandestinement ?&nbsp;&raquo; demanda le serveur. L&rsquo;homme secoua la t&ecirc;te.&nbsp; &laquo;&nbsp; Alors pourquoi n&rsquo;avez&nbsp; vous pas mang&eacute;&nbsp;?&nbsp;&raquo; Les frais de votre ticket couvrent vos repas. Vous avez d&eacute;j&agrave; pay&eacute; pour &ccedil;a. Vous avez juste besoin de venir manger.<br />
<br />
Vivons-nous comme des clandestins spirituels alors que nous sommes en droit de revendiquer tous les avantages d&rsquo;un passager de premi&egrave;re classe&nbsp;?&nbsp; Combien cela est triste de nous satisfaire d&rsquo;un Christianisme fromage-et-biscuit&nbsp; alors que J&eacute;sus nous invite &agrave; &laquo;&nbsp;venir souper&nbsp;&raquo; avec Lui &agrave; la table d&rsquo;honneur.<br />
<br />
Est-ce possible que vous croyiez en Dieu et que vous Lui avez donn&eacute; votre vie, et que pourtant vous continuez &agrave; vivre comme s&rsquo;Il n&rsquo;existe pas&nbsp;? Lui avez-vous demand&eacute; de vous guider puis vous continuez votre chemin comme s&rsquo;Il ne s&rsquo;int&eacute;resse pas &agrave; votre vie&nbsp;? Etes-vous pr&ecirc;ts &agrave; op&eacute;rer un changement et &agrave; commencer &agrave; d&eacute;pendre de la puissance prodigieuse du Saint-Esprit&nbsp;? Il vous invite &agrave; venir &agrave; ce tournant d&eacute;cisif en ce moment m&ecirc;me.<br />
<br />
Tout ce qu&rsquo;il faut, c&rsquo;est la foi&nbsp;: avoir confiance que Dieu est ce qu&rsquo;Il affirme &ecirc;tre. J&eacute;sus a dit que nous serions m&ecirc;me capables de faire des &oelig;uvres plus grandes que ceux qu&rsquo;Il avait faites si nous croyons qu&rsquo;Il&nbsp; tient sinc&egrave;rement &agrave; ce qu&rsquo;Il dit (Jean 14&nbsp;:12)&nbsp; Tout ce que nous demanderons en Son nom, Il a dit qu&rsquo;Il le fera (Jean 14:14). Il n&rsquo;est pas n&eacute;cessaire que vous viviez une vie de d&eacute;faite, charnelle, conduite par la culpabilit&eacute;. Vous avez le choix.<br />
<br />
Notre Dieu d&rsquo;amour nous ordonne de nous d&eacute;tacher de notre vie charnelle&nbsp; et de devenir les t&eacute;moins qui portent de fruit, que nous sommes appel&eacute; &agrave; &ecirc;tre en Jean 15&nbsp;:16. Le plus beau, c&rsquo;est que Lui-m&ecirc;me a aussi bien le&nbsp; pouvoir que le d&eacute;sir de nous amener &agrave; vivre&nbsp; l&rsquo;amour et le pardon v&eacute;ritables de Dieu en Lui.<br />
<br />
Et ainsi, aussi faible que soit&nbsp; notre foi, nous commen&ccedil;ons &agrave; la placer en un Dieu digne de confiance. C&rsquo;est le premier pas vers la croissance. Comme un muscle, la foi doit &ecirc;tre exerc&eacute;e si elle aspire &agrave; devenir forte et utile.<br />
<br />
Nous sommes comme l&rsquo;homme qui se d&eacute;place avec une &eacute;norme prudence &agrave; travers un lac gel&eacute; pendant un froid hivernal.&nbsp; Au d&eacute;part, il craint que ses pieds, &agrave; son prochain pas,&nbsp; n&rsquo;aillent pas quelque peu en d&eacute;ca de la plaque de l&rsquo;eau sombre&nbsp; et gel&eacute;e. Mais chaque pas qui supportait son poids confirme et renforce sa conviction selon laquelle&nbsp; la plaque de glace supportera son poids. Quand nous pla&ccedil;ons notre confiance en Dieu, le r&eacute;sultat sera toujours une foi plus forte, car mieux nous Le connaissons, plus nous savons qu&rsquo;Il m&eacute;rite notre confiance.<br />
<br />
D&rsquo;autres choses--- apparemment insignifiantes&mdash; ont un effet surprenant sur notre foi &agrave; mesure que cette derni&egrave;re devient mature. J&rsquo;ai eu une d&eacute;monstration m&eacute;morable de ceci un apr&egrave;s-midi alors que je m&rsquo;amusais avec mon petit gar&ccedil;on. C&rsquo;&eacute;tait son tour de manipuler les commandes de son&nbsp; train en miniature et, et pendant plusieurs minutes nous avons appr&eacute;ci&eacute; les bouff&eacute;s que l&acirc;chait la magnifique petite locomotive autour des collines et les vall&eacute;es imaginaires comme pr&eacute;vu. Puis sans raison apparente, elle s&rsquo;est arr&ecirc;t&eacute;e. Il a essay&eacute; encore le commutateur mais rien ne s&rsquo;est pass&eacute;. Je retirai la petite locomotive de la piste et v&eacute;rifiai la connexion. Je rebranchai la fiche dans la prise. Tout semble &ecirc;tre normal, mais le train refusa de bouger. C&rsquo;est alors que mon gar&ccedil;on a remarqu&eacute; un panneau de signalisation qui &eacute;tait tomb&eacute;e &agrave; un croisement. Bien qu&rsquo;elle ne soit pas tr&egrave;s grande, elle &eacute;tait tomb&eacute;e sur la piste, reliant les rails positif et n&eacute;gatif et rendant le train immobile. Le petit panneau avait court-circuit&eacute; le courant.<br />
<br />
Le p&eacute;ch&eacute;&mdash;m&ecirc;me un p&eacute;ch&eacute; &laquo;&nbsp;banal&nbsp;&raquo;&mdash; peut causer&nbsp; la m&ecirc;me chose dans la vie d&rsquo;un Chr&eacute;tien. Cela ne peut jamais affecter l&rsquo;amour que Dieu a pour nous. Cela ne change jamais! Dieu nous aime d&rsquo;un amour in&eacute;puisable. Il nous aime non&nbsp; seulement &laquo;&nbsp;quand&nbsp;&raquo; ou &laquo;&nbsp;si&nbsp;&raquo; nous m&eacute;ritons Son amour, mais quand&nbsp; m&ecirc;me nous sommes d&eacute;sob&eacute;issants. L&rsquo;une de mes d&eacute;couvertes les plus &eacute;mouvantes lors de mon &eacute;tude des Ecritures &eacute;tait la d&eacute;claration de notre Seigneur&nbsp; dans Sa pri&egrave;re sacerdotale&nbsp; adress&eacute;e &agrave; Dieu le P&egrave;re, comme rapport&eacute; en Jean 17&nbsp;:23 (LSG) &laquo;&nbsp;moi en eux, et toi en moi, afin qu&rsquo;ils soient parfaitement un, et que le monde connaisse que tu&nbsp; m&rsquo;as envoy&eacute; et que tu les as aim&eacute;s comme tu m&rsquo;as aim&eacute;.&nbsp;&raquo;<br />
<br />
Pensez &agrave; cela&nbsp;: Dieu nous aime vous et moi autant qu&rsquo;Il aime le Seigneur J&eacute;sus-Christ, Son Fils unique. Incroyable&nbsp;! Mais vrai&nbsp;! Bien que Dieu haie le p&eacute;ch&eacute;&nbsp; et ch&acirc;tiera ou punira Ses enfants quand nous sommes d&eacute;sob&eacute;issants, Il ne cesse jamais de nous aimer. &laquo;&nbsp;Le Seigneur ch&acirc;tie celui qu&rsquo;il aime &raquo; (H&eacute;breux 12&nbsp;:6).&nbsp; En fait, Il nous discipline parce qu&rsquo;Il nous aime, pas parce qu&rsquo;il nous haie. Il haie seulement notre p&eacute;ch&eacute;.<br />
<br />
Si donc nous voulons que Sa puissance coule incessamment &agrave; travers&nbsp; nos vies, c&rsquo;est notre responsabilit&eacute; de confesser tout p&eacute;ch&eacute; connu. Alors, nous pouvons vivre &agrave; nouveau le pardon de Dieu &agrave; cause de la mort de J&eacute;sus &agrave; notre place. La confession est aussi n&eacute;cessaire et naturelle pour une vie Chr&eacute;tienne normale que la respiration pour notre existence physique.</p>

<h2>Respiration Spirituelle</h2>

<p>En fait , c&rsquo;est respirer&mdash;respirer spirituellement. Nous &laquo;&nbsp;exhalons&nbsp;&raquo; en faisant sortir une confession vers Dieu, en expulsant le p&eacute;ch&eacute; qui est dans nos vies. Nous &laquo;&nbsp;inhalons&nbsp;&raquo; comme nous respirons dans&nbsp; le Saint-Esprit, nous-nous approprions&nbsp; Sa pl&eacute;nitude par la foi.&nbsp;&nbsp; La respiration spirituelle est un principe qui nous rend capable de vivre des vies Chr&eacute;tiennes harmonieuses. C&rsquo;est la &laquo;&nbsp;respiration de la vie&nbsp;&raquo;<br />
<br />
Consid&eacute;rez avec moi les principes de &laquo;&nbsp;l&rsquo;expiration&nbsp;&raquo; spirituelle tels qu&rsquo;ils se rapportent &agrave; la vie Chr&eacute;tienne. (Nous discuterons du processus de &laquo;&nbsp;l&rsquo;inspiration&nbsp;&raquo; spirituelle dans le prochain chapitre.) Nous lisons en 1 Jean 1&nbsp;:9&nbsp; &laquo;&nbsp;Si nous confessons nos p&eacute;ch&eacute;s, Il [Dieu] est fid&egrave;le et juste pour nous les pardonner et nous purifier de toute iniquit&eacute;&nbsp;&raquo; Le mot <em>confesser</em> ( dans le Grec, <em>homologeo</em>) sugg&egrave;re un accord avec Dieu en ce qui concerne nos p&eacute;ch&eacute;s. La confession est un processus &agrave; trois temps:</p>

<ol>
	<li>La Reconnaissance de notre p&eacute;ch&eacute; Nous avons besoin d&rsquo;&ecirc;tre pr&eacute;cis&nbsp; devant Dieu&nbsp; au sujet de&nbsp; notre&nbsp; p&eacute;ch&eacute;&nbsp; et nous mettre d&rsquo;accord avec Lui sur&nbsp; le fait que&nbsp; ce que nous avons fait est mauvais et grave &agrave; Ses yeux.&nbsp;</li>
	<li>L&rsquo;Acceptation de Son Pardon Nous devons aussi nous mettre d&rsquo;accord&nbsp; avec Dieu que&nbsp; la mort de J&eacute;sus sur la croix&nbsp; a acquis tout le pardon dont nous avons besoin pour tous nos p&eacute;ch&eacute;s&mdash;pass&eacute;, pr&eacute;sent et futur, accepter le fait que nous n&rsquo;avons rien &agrave; ajouter&nbsp; &agrave; ce qu&rsquo;il a fait pour nous.</li>
	<li>La Repentance Nous devons nous repentir, nous devons changer notre attitude vis-&agrave;-vis du p&eacute;ch&eacute;. Le Saint-Esprit nous offre la puissance dont nous avons besoin et, quand nous acceptons Sa puissance, notre conduite changera. Notre nature de p&eacute;ch&eacute; n&rsquo;est plus au commande. Elle est impuissante sous l&rsquo;autorit&eacute; de l&rsquo;Esprit Saint.&nbsp; Nous sommes&nbsp; une fois&nbsp; encore libres de&nbsp; faire ce que Dieu veut que nous fassions.</li>
</ol>

<p>Si vous souhaitez respirer spirituellement,&nbsp; il y a un simple exercice que vous pouvez faire maintenant&nbsp; et qui vous aidera.<br />
<br />
Humiliez-vous devant Dieu et demandez &agrave; l&rsquo;Esprit-Saint de vous r&eacute;v&eacute;ler le p&eacute;ch&eacute; qui est dans votre vie. Un crayon et un papier &agrave; la main, faites une liste de&nbsp; tous les p&eacute;ch&eacute;s qu&rsquo;Il rappelle &agrave; votre m&eacute;moire. Accordez-Lui un temps suffisant pour qu&rsquo;Il puisse vous montrer les domaines de votre vie qui ont besoin de changement. M&eacute;ditez le Psaume 32&nbsp;:1-6 &laquo;&nbsp;Sonde-moi, &ocirc; Dieu&nbsp;! et connais mon c&oelig;ur&nbsp;; &eacute;prouve-moi, et connais mes pens&eacute;es.&nbsp;&raquo; (LSG) .<br />
<br />
Quand vous aurez achev&eacute; de faire votre liste, &eacute;crivez horizontalement en haut la promesse ind&eacute;l&eacute;bile de 1 Jean 1&nbsp;:9&nbsp;:<em> Si nous confessons nos p&eacute;ch&eacute;s, Il [Dieu] est fid&egrave;le et juste pour nous les pardonner et nous purifier de toute iniquit&eacute;!</em><br />
<br />
D&eacute;truisez maintenant votre liste et remerciez&nbsp; Dieu pour Son pardon et Sa purification &agrave; travers la mort de Son Fils sur la croix. Son sang pr&eacute;cieux a &eacute;t&eacute; vers&eacute; pour vos p&eacute;ch&eacute;s.<br />
<br />
Garder les canaux ouverts pour que la puissance de Dieu&nbsp; puisse couler &agrave; travers&nbsp; nous, nous permet de vivre l&rsquo;amour et le pardon&nbsp; dans notre marche Chr&eacute;tienne. C&rsquo;est l&rsquo;ingr&eacute;dient qui fait des hommes et femmes ordinaires des disciples extraordinaires et dynamique s de J&eacute;sus-Christ!</p>

<h2>Application</h2>

<ol>
	<li>Qu&rsquo;avez-vous aim&eacute; le plus (qu&rsquo;est-ce qui a retenu votre attention)?</li>
	<li>Pourquoi?</li>
	<li>A qui devrais-je transmettre cette information ?</li>
</ol>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note1Text')"
        id="note1Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<p>Adapt&eacute; de Les Messages Transmissibles par Bill Bright. &copy; Cru. Tous droits r&eacute;serv&eacute;s</p>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'L\'amour et le pardon de Dieu: ', '/content/M2/fra/tc/ct02.html')">
				<img class="social" src="@/assets/sites/mc2/images/standard/Share.png" />
			</td>
		</tr>
	</tbody>
</table>
<div class="footer">
<p class="footer">MC2</p>
<p class="footer" @click="share('website', 'https://GlobalChurchMovements.org', '')"> GlobalChurchMovements.org</p>
</div>

<!-- end mc2 sdcard languageFooter -->
<!-- end sdcard languageFooterSingle -->

</div><!--- Created by publishPage-->

</template>
<!-- begin sdcard Footer -->
<!-- end sdcard Footer -->