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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply3-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>9.</h1></div>
                        <div class="chapter_title ltr"><h1>Le succès dans le ministère attire la persécution</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="lesson">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p><em>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</em></p>

<ul>
	<li class="nobreak-final-final">(Facultatif) J&eacute;sus-Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re ; qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;. Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus-Christ homme, qui s&rsquo;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. (<span class="popup-link" @click = "popUp('pop1')"> Philippiens 2:11</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">11&nbsp;</sup>et que toute langue confesse que J&eacute;sus Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> 1 Timoth&eacute;e 2:4-6</span>)&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">4&nbsp;</sup>qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;.</p>

	<p><sup class="versenum">5&nbsp;</sup>Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus Christ homme,</p>

	<p><sup class="versenum">6&nbsp;</sup>qui s&#39;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. C&#39;est l&agrave; le t&eacute;moignage rendu en son propre temps,</p>
	<!-- end bible --></div>
	</li>
</ul>

</div>

<h2>Soin</h2>

<p><em>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</em></p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la fid&eacute;lit&eacute;</h2>

<p><em>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</em></p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Motivation et encouragement</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p><em>Trouvez un moyen de projeter une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux:</em></p>

<ul>
	<li class="indent">un passage qui leur rappelle le c&oelig;ur du P&egrave;re et de la vision final.</li>
	<li>r&eacute;fl&eacute;chir sur des changements intervenus dans leur vie depuis qu&rsquo;ils ont commenc&eacute; &agrave; suivre Christ</li>
	<li>leur rappeler ce que Dieu veut faire &agrave; travers eux</li>
</ul>

<p><strong>Partagez la GRANDE vision</strong> <em>&laquo; une &eacute;glise pour chaque village et communaut&eacute;, l&rsquo;&eacute;vangile pour chaque personne &raquo;.</em></p>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><p>+ Contexte</p></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<ul>
	<li>Demandez au groupe de raconter l&rsquo;histoire de la semaine pass&eacute;e.</li>
</ul>

</div>

<h2>Lisez</h2>

<ul>
	<li>Lisez ou observez Actes 5:12-42 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 5:12-42</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">12&nbsp;</sup>Beaucoup de miracles et de prodiges se faisaient au milieu du peuple par les mains des ap&ocirc;tres. Ils se tenaient tous ensemble au portique de Salomon,</p>

<p><sup class="versenum">13&nbsp;</sup>et aucun des autres n&#39;osait se joindre &agrave; eux; mais le peuple les louait hautement.</p>

<p><sup class="versenum">14&nbsp;</sup>Le nombre de ceux qui croyaient au Seigneur, hommes et femmes, s&#39;augmentait de plus en plus;</p>

<p><sup class="versenum">15&nbsp;</sup>en sorte qu&#39;on apportait les malades dans les rues et qu&#39;on les pla&ccedil;ait sur des lits et des couchettes, afin que, lorsque Pierre passerait, son ombre au moins couvr&icirc;t quelqu&#39;un d&#39;eux.</p>

<p><sup class="versenum">16&nbsp;</sup>La multitude accourait aussi des villes voisines &agrave; J&eacute;rusalem, amenant des malades et des gens tourment&eacute;s par des esprits impurs; et tous &eacute;taient gu&eacute;ris.</p>

<p><sup class="versenum">17&nbsp;</sup>Cependant le souverain sacrificateur et tous ceux qui &eacute;taient avec lui, savoir le parti des sadduc&eacute;ens, se lev&egrave;rent, remplis de jalousie,</p>

<p><sup class="versenum">18&nbsp;</sup>mirent les mains sur les ap&ocirc;tres, et les jet&egrave;rent dans la prison publique.</p>

<p><sup class="versenum">19&nbsp;</sup>Mais un ange du Seigneur, ayant ouvert pendant la nuit les portes de la prison, les fit sortir, et leur dit:</p>

<p><sup class="versenum">20&nbsp;</sup>Allez, tenez-vous dans le temple, et annoncez au peuple toutes les paroles de cette vie.</p>

<p><sup class="versenum">21&nbsp;</sup>Ayant entendu cela, ils entr&egrave;rent d&egrave;s le matin dans le temple, et se mirent &agrave; enseigner. Le souverain sacrificateur et ceux qui &eacute;taient avec lui &eacute;tant survenus, ils convoqu&egrave;rent le sanh&eacute;drin et tous les anciens des fils d&#39;Isra&euml;l, et ils envoy&egrave;rent chercher les ap&ocirc;tres &agrave; la prison.</p>

<p><sup class="versenum">22&nbsp;</sup>Les huissiers, &agrave; leur arriv&eacute;e, ne les trouv&egrave;rent point dans la prison. Ils s&#39;en retourn&egrave;rent, et firent leur rapport,</p>

<p><sup class="versenum">23&nbsp;</sup>en disant: Nous avons trouv&eacute; la prison soigneusement ferm&eacute;e, et les gardes qui &eacute;taient devant les portes; mais, apr&egrave;s avoir ouvert, nous n&#39;avons trouv&eacute; personne dedans.</p>

<p><sup class="versenum">24&nbsp;</sup>Lorsqu&#39;ils eurent entendu ces paroles, le commandant du temple et les principaux sacrificateurs ne savaient que penser des ap&ocirc;tres et des suites de cette affaire.</p>

<p><sup class="versenum">25&nbsp;</sup>Quelqu&#39;un vint leur dire: Voici, les hommes que vous avez mis en prison sont dans le temple, et ils enseignent le peuple.</p>

<p><sup class="versenum">26&nbsp;</sup>Alors le commandant partit avec les huissiers, et les conduisit sans violence, car ils avaient peur d&#39;&ecirc;tre lapid&eacute;s par le peuple.</p>

<p><sup class="versenum">27&nbsp;</sup>Apr&egrave;s qu&#39;ils les eurent amen&eacute;s en pr&eacute;sence du sanh&eacute;drin, le souverain sacrificateur les interrogea en ces termes:</p>

<p><sup class="versenum">28&nbsp;</sup>Ne vous avons-nous pas d&eacute;fendu express&eacute;ment d&#39;enseigner en ce nom-l&agrave;? Et voici, vous avez rempli J&eacute;rusalem de votre enseignement, et vous voulez faire retomber sur nous le sang de cet homme!</p>

<p><sup class="versenum">29&nbsp;</sup>Pierre et les ap&ocirc;tres r&eacute;pondirent: Il faut ob&eacute;ir &agrave; Dieu plut&ocirc;t qu&#39;aux hommes.</p>

<p><sup class="versenum">30&nbsp;</sup>Le Dieu de nos p&egrave;res a ressuscit&eacute; J&eacute;sus, que vous avez tu&eacute;, en le pendant au bois.</p>

<p><sup class="versenum">31&nbsp;</sup>Dieu l&#39;a &eacute;lev&eacute; par sa droite comme Prince et Sauveur, pour donner &agrave; Isra&euml;l la repentance et le pardon des p&eacute;ch&eacute;s.</p>

<p><sup class="versenum">32&nbsp;</sup>Nous sommes t&eacute;moins de ces choses, de m&ecirc;me que le Saint Esprit, que Dieu a donn&eacute; &agrave; ceux qui lui ob&eacute;issent.</p>

<p><sup class="versenum">33&nbsp;</sup>Furieux de ces paroles, ils voulaient les faire mourir.</p>

<p><sup class="versenum">34&nbsp;</sup>Mais un pharisien, nomm&eacute; Gamaliel, docteur de la loi, estim&eacute; de tout le peuple, se leva dans le sanh&eacute;drin, et ordonna de faire sortir un instant les ap&ocirc;tres.</p>

<p><sup class="versenum">35&nbsp;</sup>Puis il leur dit: Hommes Isra&eacute;lites, prenez garde &agrave; ce que vous allez faire &agrave; l&#39;&eacute;gard de ces gens.</p>

<p><sup class="versenum">36&nbsp;</sup>Car, il n&#39;y a pas longtemps que parut Theudas, qui se donnait pour quelque chose, et auquel se ralli&egrave;rent environ quatre cents hommes: il fut tu&eacute;, et tous ceux qui l&#39;avaient suivi furent mis en d&eacute;route et r&eacute;duits &agrave; rien.</p>

<p><sup class="versenum">37&nbsp;</sup>Apr&egrave;s lui, parut Judas le Galil&eacute;en, &agrave; l&#39;&eacute;poque du recensement, et il attira du monde &agrave; son parti: il p&eacute;rit aussi, et tous ceux qui l&#39;avaient suivi furent dispers&eacute;s.</p>

<p><sup class="versenum">38&nbsp;</sup>Et maintenant, je vous le dis ne vous occupez plus de ces hommes, et laissez-les aller. Si cette entreprise ou cette oeuvre vient des hommes, elle se d&eacute;truira;</p>

<p><sup class="versenum">39&nbsp;</sup>mais si elle vient de Dieu, vous ne pourrez la d&eacute;truire. Ne courez pas le risque d&#39;avoir combattu contre Dieu.</p>

<p><sup class="versenum">40&nbsp;</sup>Ils se rang&egrave;rent &agrave; son avis. Et ayant appel&eacute; les ap&ocirc;tres, ils les firent battre de verges, ils leur d&eacute;fendirent de parler au nom de J&eacute;sus, et ils les rel&acirc;ch&egrave;rent.</p>

<p><sup class="versenum">41&nbsp;</sup>Les ap&ocirc;tres se retir&egrave;rent de devant le sanh&eacute;drin, joyeux d&#39;avoir &eacute;t&eacute; jug&eacute;s dignes de subir des outrages pour le nom de J&eacute;sus.</p>

<p><sup class="versenum">42&nbsp;</sup>Et chaque jour, dans le temple et dans les maisons, ils ne cessaient d&#39;enseigner, et d&#39;annoncer la bonne nouvelle de J&eacute;sus Christ.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/309.mp4" type="button" class="external-movie">
         Regardez Actes 5:12-42 </button>
    <div class="collapsed"></div>




<h2>Discussion de d&eacute;couverte</h2>

<ul>
	<li>Qu&rsquo;est-ce qui a retenu votre attention ou qu&rsquo;avez-vous aim&eacute; le plus ? Pourquoi ?</li>
	<li>&Agrave; ce niveau de l&rsquo;histoire, qu&rsquo;est-ce qui est nouveau ou est d&eacute;velopp&eacute; ?</li>
	<li>Quel mod&egrave;le a &eacute;t&eacute; donn&eacute; quant &agrave; la vie d&eacute;pendante de l&rsquo;Esprit, faire de disciples ou au leadership ?</li>
	<li>Comment pouvons-nous vivre diff&eacute;remment maintenant que nous connaissons cette histoire?</li>
</ul>

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


<p><em>Des questions suppl&eacute;mentaires dont vous pouvez faire usage:</em></p>

<ul>
	<li>Comment les disciples de J&eacute;sus poursuivent-ils Son &oelig;uvre de faire des disciples et d&rsquo;implantation d&rsquo;&eacute;glises ?</li>
	<li>Comment l&rsquo;&eacute;vangile impacte-t-il les gens et la soci&eacute;t&eacute; ?</li>
	<li>Quels &eacute;taient les barri&egrave;res et les obstacles qui ont &eacute;t&eacute; surmont&eacute;s et comment ont-ils &eacute;t&eacute; surmont&eacute;s ?</li>
</ul>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note2Text')"
        id="note2Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<h2>Lire, raconter et corriger</h2>

<p>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</p>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<ul>
	<li class="nobreak-final-final">Les croyants avaient une bonne r&eacute;putation au milieu des gens qui vivaient &agrave; J&eacute;rusalem. Beaucoup de villages et villes voisins &eacute;taient attir&eacute;s par le minist&egrave;re de l&#39;&eacute;glise de J&eacute;rusalem. Les ap&ocirc;tres vivaient ce pour quoi ils avaient &eacute;t&eacute; form&eacute;s par J&eacute;sus: gu&eacute;rir les malades, chasser les d&eacute;mons et pr&ecirc;cher la bonne nouvelle du Royaume (<span class="popup-link" @click = "popUp('pop3')"> Matthieu 10</span>,&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<div>
	<div>
	<div>
	<div>
	<div>
	<div>
	<p><sup class="versenum">1 </sup>Puis, ayant appel&eacute; ses douze disciples, il leur donna le pouvoir de chasser les esprits impurs, et de gu&eacute;rir toute maladie et toute infirmit&eacute;.</p>

	<p><sup class="versenum">2&nbsp;</sup>Voici les noms des douze ap&ocirc;tres. Le premier, Simon appel&eacute; Pierre, et Andr&eacute;, son fr&egrave;re; Jacques, fils de Z&eacute;b&eacute;d&eacute;e, et Jean, son fr&egrave;re;</p>

	<p><sup class="versenum">3&nbsp;</sup>Philippe, et Barth&eacute;lemy; Thomas, et Matthieu, le publicain; Jacques, fils d&#39;Alph&eacute;e, et Thadd&eacute;e;</p>

	<p><sup class="versenum">4&nbsp;</sup>Simon le Cananite, et Judas l&#39;Iscariot, celui qui livra J&eacute;sus.</p>

	<p><sup class="versenum">5&nbsp;</sup>Tels sont les douze que J&eacute;sus envoya, apr&egrave;s leur avoir donn&eacute; les instructions suivantes: N&#39;allez pas vers les pa&iuml;ens, et n&#39;entrez pas dans les villes des Samaritains;</p>

	<p><sup class="versenum">6&nbsp;</sup>allez plut&ocirc;t vers les brebis perdues de la maison d&#39;Isra&euml;l.</p>

	<p><sup class="versenum">7&nbsp;</sup>Allez, pr&ecirc;chez, et dites: Le royaume des cieux est proche.</p>

	<p><sup class="versenum">8&nbsp;</sup>Gu&eacute;rissez les malades, ressuscitez les morts, purifiez les l&eacute;preux, chassez les d&eacute;mons. Vous avez re&ccedil;u gratuitement, donnez gratuitement.</p>

	<p><sup class="versenum">9&nbsp;</sup>Ne prenez ni or, ni argent, ni monnaie, dans vos ceintures;</p>

	<p><sup class="versenum">10&nbsp;</sup>ni sac pour le voyage, ni deux tuniques, ni souliers, ni b&acirc;ton; car l&#39;ouvrier m&eacute;rite sa nourriture.</p>

	<p><sup class="versenum">11&nbsp;</sup>Dans quelque ville ou village que vous entriez, informez-vous s&#39;il s&#39;y trouve quelque homme digne de vous recevoir; et demeurez chez lui jusqu&#39;&agrave; ce que vous partiez.</p>

	<p><sup class="versenum">12&nbsp;</sup>En entrant dans la maison, saluez-la;</p>

	<p><sup class="versenum">13&nbsp;</sup>et, si la maison en est digne, que votre paix vienne sur elle; mais si elle n&#39;en est pas digne, que votre paix retourne &agrave; vous.</p>

	<p><sup class="versenum">14&nbsp;</sup>Lorsqu&#39;on ne vous recevra pas et qu&#39;on n&#39;&eacute;coutera pas vos paroles, sortez de cette maison ou de cette ville et secouez la poussi&egrave;re de vos pieds.</p>

	<p><sup class="versenum">15&nbsp;</sup>Je vous le dis en v&eacute;rit&eacute;: au jour du jugement, le pays de Sodome et de Gomorrhe sera trait&eacute; moins rigoureusement que cette ville-l&agrave;.</p>

	<p><sup class="versenum">16&nbsp;</sup>Voici, je vous envoie comme des brebis au milieu des loups. Soyez donc prudents comme les serpents, et simples comme les colombes.</p>

	<p><sup class="versenum">17&nbsp;</sup>Mettez-vous en garde contre les hommes; car ils vous livreront aux tribunaux, et ils vous battront de verges dans leurs synagogues;</p>

	<p><sup class="versenum">18&nbsp;</sup>vous serez men&eacute;s, &agrave; cause de moi, devant des gouverneurs et devant des rois, pour servir de t&eacute;moignage &agrave; eux et aux pa&iuml;ens.</p>

	<p><sup class="versenum">19&nbsp;</sup>Mais, quand on vous livrera, ne vous inqui&eacute;tez ni de la mani&egrave;re dont vous parlerez ni de ce que vous direz: ce que vous aurez &agrave; dire vous sera donn&eacute; &agrave; l&#39;heure m&ecirc;me;</p>

	<p><sup class="versenum">20&nbsp;</sup>car ce n&#39;est pas vous qui parlerez, c&#39;est l&#39;Esprit de votre P&egrave;re qui parlera en vous.</p>

	<p><sup class="versenum">21&nbsp;</sup>Le fr&egrave;re livrera son fr&egrave;re &agrave; la mort, et le p&egrave;re son enfant; les enfants se soul&egrave;veront contre leurs parents, et les feront mourir.</p>

	<p><sup class="versenum">22&nbsp;</sup>Vous serez ha&iuml;s de tous, &agrave; cause de mon nom; mais celui qui pers&eacute;v&eacute;rera jusqu&#39;&agrave; la fin sera sauv&eacute;.</p>

	<p><sup class="versenum">23&nbsp;</sup>Quand on vous pers&eacute;cutera dans une ville, fuyez dans une autre. Je vous le dis en v&eacute;rit&eacute;, vous n&#39;aurez pas achev&eacute; de parcourir les villes d&#39;Isra&euml;l que le Fils de l&#39;homme sera venu.</p>

	<p><sup class="versenum">24&nbsp;</sup>Le disciple n&#39;est pas plus que le ma&icirc;tre, ni le serviteur plus que son seigneur.</p>

	<p><sup class="versenum">25&nbsp;</sup>Il suffit au disciple d&#39;&ecirc;tre trait&eacute; comme son ma&icirc;tre, et au serviteur comme son seigneur. S&#39;ils ont appel&eacute; le ma&icirc;tre de la maison B&eacute;elz&eacute;bul, &agrave; combien plus forte raison appelleront-ils ainsi les gens de sa maison!</p>

	<p><sup class="versenum">26&nbsp;</sup>Ne les craignez donc point; car il n&#39;y a rien de cach&eacute; qui ne doive &ecirc;tre d&eacute;couvert, ni de secret qui ne doive &ecirc;tre connu.</p>

	<p><sup class="versenum">27&nbsp;</sup>Ce que je vous dis dans les t&eacute;n&egrave;bres, dites-le en plein jour; et ce qui vous est dit &agrave; l&#39;oreille, pr&ecirc;chez-le sur les toits.</p>

	<p><sup class="versenum">28&nbsp;</sup>Ne craignez pas ceux qui tuent le corps et qui ne peuvent tuer l&#39;&acirc;me; craignez plut&ocirc;t celui qui peut faire p&eacute;rir l&#39;&acirc;me et le corps dans la g&eacute;henne.</p>

	<p><sup class="versenum">29&nbsp;</sup>Ne vend-on pas deux passereaux pour un sou? Cependant, il n&#39;en tombe pas un &agrave; terre sans la volont&eacute; de votre P&egrave;re.</p>

	<p><sup class="versenum">30&nbsp;</sup>Et m&ecirc;me les cheveux de votre t&ecirc;te sont tous compt&eacute;s.</p>

	<p><sup class="versenum">31&nbsp;</sup>Ne craignez donc point: vous valez plus que beaucoup de passereaux.</p>

	<p><sup class="versenum">32&nbsp;</sup>C&#39;est pourquoi, quiconque me confessera devant les hommes, je le confesserai aussi devant mon P&egrave;re qui est dans les cieux;</p>

	<p><sup class="versenum">33&nbsp;</sup>mais quiconque me reniera devant les hommes, je le renierai aussi devant mon P&egrave;re qui est dans les cieux.</p>

	<p><sup class="versenum">34&nbsp;</sup>Ne croyez pas que je sois venu apporter la paix sur la terre; je ne suis pas venu apporter la paix, mais l&#39;&eacute;p&eacute;e.</p>

	<p><sup class="versenum">35&nbsp;</sup>Car je suis venu mettre la division entre l&#39;homme et son p&egrave;re, entre la fille et sa m&egrave;re, entre la belle-fille et sa belle-m&egrave;re;</p>

	<p><sup class="versenum">36&nbsp;</sup>et l&#39;homme aura pour ennemis les gens de sa maison.</p>

	<p><sup class="versenum">37&nbsp;</sup>Celui qui aime son p&egrave;re ou sa m&egrave;re plus que moi n&#39;est pas digne de moi, et celui qui aime son fils ou sa fille plus que moi n&#39;est pas digne de moi;</p>

	<p><sup class="versenum">38&nbsp;</sup>celui qui ne prend pas sa croix, et ne me suit pas, n&#39;est pas digne de moi.</p>

	<p><sup class="versenum">39&nbsp;</sup>Celui qui conservera sa vie la perdra, et celui qui perdra sa vie &agrave; cause de moi la retrouvera.</p>

	<p><sup class="versenum">40&nbsp;</sup>Celui qui vous re&ccedil;oit me re&ccedil;oit, et celui qui me re&ccedil;oit, re&ccedil;oit celui qui m&#39;a envoy&eacute;.</p>

	<p><sup class="versenum">41&nbsp;</sup>Celui qui re&ccedil;oit un proph&egrave;te en qualit&eacute; de proph&egrave;te recevra une r&eacute;compense de proph&egrave;te, et celui qui re&ccedil;oit un juste en qualit&eacute; de juste recevra une r&eacute;compense de juste.</p>

	<p><sup class="versenum">42&nbsp;</sup>Et quiconque donnera seulement un verre d&#39;eau froide &agrave; l&#39;un de ces petits parce qu&#39;il est mon disciple, je vous le dis en v&eacute;rit&eacute;, il ne perdra point sa r&eacute;compense.</p>
	</div>
	</div>
	</div>
	</div>
	</div>
	</div>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop4')"> Luc 10</span>).&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<div>
	<div>
	<div>
	<div>
	<div>
	<div>
	<p><sup class="versenum">1 </sup>Apr&egrave;s cela, le Seigneur d&eacute;signa encore soixante-dix autres disciples, et il les envoya deux &agrave; deux devant lui dans toutes les villes et dans tous les lieux o&ugrave; lui-m&ecirc;me devait aller.</p>

	<p><sup class="versenum">2&nbsp;</sup>Il leur dit: La moisson est grande, mais il y a peu d&#39;ouvriers. Priez donc le ma&icirc;tre de la moisson d&#39;envoyer des ouvriers dans sa moisson.</p>

	<p><sup class="versenum">3&nbsp;</sup>Partez; voici, je vous envoie comme des agneaux au milieu des loups.</p>

	<p><sup class="versenum">4&nbsp;</sup>Ne portez ni bourse, ni sac, ni souliers, et ne saluez personne en chemin.</p>

	<p><sup class="versenum">5&nbsp;</sup>Dans quelque maison que vous entriez, dites d&#39;abord: Que la paix soit sur cette maison!</p>

	<p><sup class="versenum">6&nbsp;</sup>Et s&#39;il se trouve l&agrave; un enfant de paix, votre paix reposera sur lui; sinon, elle reviendra &agrave; vous.</p>

	<p><sup class="versenum">7&nbsp;</sup>Demeurez dans cette maison-l&agrave;, mangeant et buvant ce qu&#39;on vous donnera; car l&#39;ouvrier m&eacute;rite son salaire. N&#39;allez pas de maison en maison.</p>

	<p><sup class="versenum">8&nbsp;</sup>Dans quelque ville que vous entriez, et o&ugrave; l&#39;on vous recevra, mangez ce qui vous sera pr&eacute;sent&eacute;,</p>

	<p><sup class="versenum">9&nbsp;</sup>gu&eacute;rissez les malades qui s&#39;y trouveront, et dites-leur: Le royaume de Dieu s&#39;est approch&eacute; de vous.</p>

	<p><sup class="versenum">10&nbsp;</sup>Mais dans quelque ville que vous entriez, et o&ugrave; l&#39;on ne vous recevra pas, allez dans ses rues, et dites:</p>

	<p><sup class="versenum">11&nbsp;</sup>Nous secouons contre vous la poussi&egrave;re m&ecirc;me de votre ville qui s&#39;est attach&eacute;e &agrave; nos pieds; sachez cependant que le royaume de Dieu s&#39;est approch&eacute;.</p>

	<p><sup class="versenum">12&nbsp;</sup>Je vous dis qu&#39;en ce jour Sodome sera trait&eacute;e moins rigoureusement que cette ville-l&agrave;.</p>

	<p><sup class="versenum">13&nbsp;</sup>Malheur &agrave; toi, Chorazin! malheur &agrave; toi, Bethsa&iuml;da! car, si les miracles qui ont &eacute;t&eacute; faits au milieu de vous avaient &eacute;t&eacute; faits dans Tyr et dans Sidon, il y a longtemps qu&#39;elles se seraient repenties, en prenant le sac et la cendre.</p>

	<p><sup class="versenum">14&nbsp;</sup>C&#39;est pourquoi, au jour du jugement, Tyr et Sidon seront trait&eacute;es moins rigoureusement que vous.</p>

	<p><sup class="versenum">15&nbsp;</sup>Et toi, Caperna&uuml;m, qui as &eacute;t&eacute; &eacute;lev&eacute;e jusqu&#39;au ciel, tu seras abaiss&eacute;e jusqu&#39;au s&eacute;jour des morts.</p>

	<p><sup class="versenum">16&nbsp;</sup>Celui qui vous &eacute;coute m&#39;&eacute;coute, et celui qui vous rejette me rejette; et celui qui me rejette rejette celui qui m&#39;a envoy&eacute;.</p>

	<p><sup class="versenum">17&nbsp;</sup>Les soixante-dix revinrent avec joie, disant: Seigneur, les d&eacute;mons m&ecirc;mes nous sont soumis en ton nom.</p>

	<p><sup class="versenum">18&nbsp;</sup>J&eacute;sus leur dit: Je voyais Satan tomber du ciel comme un &eacute;clair.</p>

	<p><sup class="versenum">19&nbsp;</sup>Voici, je vous ai donn&eacute; le pouvoir de marcher sur les serpents et les scorpions, et sur toute la puissance de l&#39;ennemi; et rien ne pourra vous nuire.</p>

	<p><sup class="versenum">20&nbsp;</sup>Cependant, ne vous r&eacute;jouissez pas de ce que les esprits vous sont soumis; mais r&eacute;jouissez-vous de ce que vos noms sont &eacute;crits dans les cieux.</p>

	<p><sup class="versenum">21&nbsp;</sup>En ce moment m&ecirc;me, J&eacute;sus tressaillit de joie par le Saint Esprit, et il dit: Je te loue, P&egrave;re, Seigneur du ciel et de la terre, de ce que tu as cach&eacute; ces choses aux sages et aux intelligents, et de ce que tu les as r&eacute;v&eacute;l&eacute;es aux enfants. Oui, P&egrave;re, je te loue de ce que tu l&#39;as voulu ainsi.</p>

	<p><sup class="versenum">22&nbsp;</sup>Toutes choses m&#39;ont &eacute;t&eacute; donn&eacute;es par mon P&egrave;re, et personne ne conna&icirc;t qui est le Fils, si ce n&#39;est le P&egrave;re, ni qui est le P&egrave;re, si ce n&#39;est le Fils et celui &agrave; qui le Fils veut le r&eacute;v&eacute;ler.</p>

	<p><sup class="versenum">23&nbsp;</sup>Et, se tournant vers les disciples, il leur dit en particulier: Heureux les yeux qui voient ce que vous voyez!</p>

	<p><sup class="versenum">24&nbsp;</sup>Car je vous dis que beaucoup de proph&egrave;tes et de rois ont d&eacute;sir&eacute; voir ce que vous voyez, et ne l&#39;ont pas vu, entendre ce que vous entendez, et ne l&#39;ont pas entendu.</p>

	<p><sup class="versenum">25&nbsp;</sup>Un docteur de la loi se leva, et dit &agrave; J&eacute;sus, pour l&#39;&eacute;prouver: Ma&icirc;tre, que dois-je faire pour h&eacute;riter la vie &eacute;ternelle?</p>

	<p><sup class="versenum">26&nbsp;</sup>J&eacute;sus lui dit: Qu&#39;est-il &eacute;crit dans la loi? Qu&#39;y lis-tu?</p>

	<p><sup class="versenum">27&nbsp;</sup>Il r&eacute;pondit: Tu aimeras le Seigneur, ton Dieu, de tout ton coeur, de toute ton &acirc;me, de toute ta force, et de toute ta pens&eacute;e; et ton prochain comme toi-m&ecirc;me.</p>

	<p><sup class="versenum">28&nbsp;</sup>Tu as bien r&eacute;pondu, lui dit J&eacute;sus; fais cela, et tu vivras.</p>

	<p><sup class="versenum">29&nbsp;</sup>Mais lui, voulant se justifier, dit &agrave; J&eacute;sus: Et qui est mon prochain?</p>

	<p><sup class="versenum">30&nbsp;</sup>J&eacute;sus reprit la parole, et dit: Un homme descendait de J&eacute;rusalem &agrave; J&eacute;richo. Il tomba au milieu des brigands, qui le d&eacute;pouill&egrave;rent, le charg&egrave;rent de coups, et s&#39;en all&egrave;rent, le laissant &agrave; demi mort.</p>

	<p><sup class="versenum">31&nbsp;</sup>Un sacrificateur, qui par hasard descendait par le m&ecirc;me chemin, ayant vu cet homme, passa outre.</p>

	<p><sup class="versenum">32&nbsp;</sup>Un L&eacute;vite, qui arriva aussi dans ce lieu, l&#39;ayant vu, passa outre.</p>

	<p><sup class="versenum">33&nbsp;</sup>Mais un Samaritain, qui voyageait, &eacute;tant venu l&agrave;, fut &eacute;mu de compassion lorsqu&#39;il le vit.</p>

	<p><sup class="versenum">34&nbsp;</sup>Il s&#39;approcha, et banda ses plaies, en y versant de l&#39;huile et du vin; puis il le mit sur sa propre monture, le conduisit &agrave; une h&ocirc;tellerie, et prit soin de lui.</p>

	<p><sup class="versenum">35&nbsp;</sup>Le lendemain, il tira deux deniers, les donna &agrave; l&#39;h&ocirc;te, et dit: Aie soin de lui, et ce que tu d&eacute;penseras de plus, je te le rendrai &agrave; mon retour.</p>

	<p><sup class="versenum">36&nbsp;</sup>Lequel de ces trois te semble avoir &eacute;t&eacute; le prochain de celui qui &eacute;tait tomb&eacute; au milieu des brigands?</p>

	<p><sup class="versenum">37&nbsp;</sup>C&#39;est celui qui a exerc&eacute; la mis&eacute;ricorde envers lui, r&eacute;pondit le docteur de la loi. Et J&eacute;sus lui dit: Va, et toi, fais de m&ecirc;me.</p>

	<p><sup class="versenum">38&nbsp;</sup>Comme J&eacute;sus &eacute;tait en chemin avec ses disciples, il entra dans un village, et une femme, nomm&eacute;e Marthe, le re&ccedil;ut dans sa maison.</p>

	<p><sup class="versenum">39&nbsp;</sup>Elle avait une soeur, nomm&eacute;e Marie, qui, s&#39;&eacute;tant assise aux pieds du Seigneur, &eacute;coutait sa parole.</p>

	<p><sup class="versenum">40&nbsp;</sup>Marthe, occup&eacute;e &agrave; divers soins domestiques, survint et dit: Seigneur, cela ne te fait-il rien que ma soeur me laisse seule pour servir? Dis-lui donc de m&#39;aider.</p>

	<p><sup class="versenum">41&nbsp;</sup>Le Seigneur lui r&eacute;pondit: Marthe, Marthe, tu t&#39;inqui&egrave;tes et tu t&#39;agites pour beaucoup de choses.</p>

	<p><sup class="versenum">42&nbsp;</sup>Une seule chose est n&eacute;cessaire. Marie a choisi la bonne part, qui ne lui sera point &ocirc;t&eacute;e.</p>
	</div>
	</div>
	</div>
	</div>
	</div>
	</div>
	<!-- end bible --></div>
	Cependant, ils ne sortaient pas de J&eacute;rusalem pour aller vers les gens comme J&eacute;sus leur avait ordonn&eacute; (<span class="popup-link" @click = "popUp('pop5')"> Actes 1: 8</span>).&nbsp;

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">8&nbsp;</sup>Mais vous recevrez une puissance, le Saint Esprit survenant sur vous, et vous serez mes t&eacute;moins &agrave; J&eacute;rusalem, dans toute la Jud&eacute;e, dans la Samarie, et jusqu&#39;aux extr&eacute;mit&eacute;s de la terre.</p>
	<!-- end bible --></div>
	Les chefs religieux ont r&eacute;agi &agrave; la popularit&eacute; croissante de cette nouvelle communaut&eacute; avec jalousie comme ils avaient r&eacute;agi &agrave; la popularit&eacute; de J&eacute;sus. Cela a conduit &agrave; la pers&eacute;cution des ap&ocirc;tres. J&eacute;sus est intervenu une fois de plus et a envoy&eacute; un ange pour les aider &agrave; s&#39;&eacute;chapper miraculeusement de la prison. Lorsqu&#39;il est &agrave; nouveau question d&rsquo;affronter les chefs religieux, Pierre insiste sur le fait qu&#39;ils doivent ob&eacute;ir &agrave; Dieu par-dessus tous. Les chefs religieux ont maintenant intensifi&eacute; leur pers&eacute;cution en y incluant la violence physique. Les ap&ocirc;tres se sont r&eacute;jouis au milieu de ces adversit&eacute;s qu&rsquo;ils ont consid&eacute;r&eacute;es comme &eacute;tant un honneur de souffrir comme J&eacute;sus.</li>
</ul>

<p>&nbsp;</p>
</div>

<p><em>Pratiquez ici la lib&eacute;ralit&eacute; et la sainte-c&egrave;ne ou dans la section Se pr&eacute;parer pour la mission.</em></p>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary4" class="summary"><h2>+ Se pr&eacute;parer pour la mission</h2></div>
<div class="collapsed" id ="Text4">
<!-- end default revealSummary -->

<p><span class="tlid-translation translation" lang="fr"><span title="">Pratiquez les comp&eacute;tences n&eacute;cessaires ou les sujets pr&eacute;c&eacute;dents pour vous pr&eacute;parer &agrave; servir les autres:</span></span></p>

<ul>
	<li><span class="tlid-translation translation" lang="fr"><span title="">Pri&egrave;re, soins, partage</span></span></li>
	<li><span class="tlid-translation translation" lang="fr"><span title="">Gospel</span></span></li>
	<li><span class="tlid-translation translation" lang="fr"><span title="">&Eacute;tudes bibliques fondamentales.</span></span></li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en mission</h2>

<ul>
	<li>Identifiez des gens vers qui ou des endroits o&ugrave; vous pouvez prendre l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>&Eacute;crivez des promesses &laquo; Je ferai d&rsquo;ici quand &raquo; et partagez cela avec votre petit groupe.</li>
</ul>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note3Text')"
        id="note3Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<h2>Prier pour la mission</h2>

<p>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples.</p>

<h2>B&eacute;n&eacute;diction (facultatif)</h2>
</div>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Le succès dans le ministère attire la persécution: ', '/content/M2/fra/multiply3/multiply309.html')">
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