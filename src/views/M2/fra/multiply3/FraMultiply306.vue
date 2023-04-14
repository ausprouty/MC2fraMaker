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
                        <div class="chapter_number ltr"><h1>6.</h1></div>
                        <div class="chapter_title ltr"><h1>Jésus utilise Pierre et Jean pour guérir un mendiant boiteux</h1></div>
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
	<span class="popup-link" @click = "popUp('pop2')"> 1 Timoth&eacute;e 2:4-6</span>)

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
	<li>Lisez ou observez Actes 3:1-26 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 3</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Pierre et Jean montaient ensemble au temple, &agrave; l&#39;heure de la pri&egrave;re: c&#39;&eacute;tait la neuvi&egrave;me heure.</p>

<p><sup class="versenum">2&nbsp;</sup>Il y avait un homme boiteux de naissance, qu&#39;on portait et qu&#39;on pla&ccedil;ait tous les jours &agrave; la porte du temple appel&eacute;e la Belle, pour qu&#39;il demand&acirc;t l&#39;aum&ocirc;ne &agrave; ceux qui entraient dans le temple.</p>

<p><sup class="versenum">3&nbsp;</sup>Cet homme, voyant Pierre et Jean qui allaient y entrer, leur demanda l&#39;aum&ocirc;ne.</p>

<p><sup class="versenum">4&nbsp;</sup>Pierre, de m&ecirc;me que Jean, fixa les yeux sur lui, et dit: Regarde-nous.</p>

<p><sup class="versenum">5&nbsp;</sup>Et il les regardait attentivement, s&#39;attendant &agrave; recevoir d&#39;eux quelque chose.</p>

<p><sup class="versenum">6&nbsp;</sup>Alors Pierre lui dit: Je n&#39;ai ni argent, ni or; mais ce que j&#39;ai, je te le donne: au nom de J&eacute;sus Christ de Nazareth, l&egrave;ve-toi et marche.</p>

<p><sup class="versenum">7&nbsp;</sup>Et le prenant par la main droite, il le fit lever. Au m&ecirc;me instant, ses pieds et ses chevilles devinrent fermes;</p>

<p><sup class="versenum">8&nbsp;</sup>d&#39;un saut il fut debout, et il se mit &agrave; marcher. Il entra avec eux dans le temple, marchant, sautant, et louant Dieu.</p>

<p><sup class="versenum">9&nbsp;</sup>Tout le monde le vit marchant et louant Dieu.</p>

<p><sup class="versenum">10&nbsp;</sup>Ils reconnaissaient que c&#39;&eacute;tait celui qui &eacute;tait assis &agrave; la Belle porte du temple pour demander l&#39;aum&ocirc;ne, et ils furent remplis d&#39;&eacute;tonnement et de surprise au sujet de ce qui lui &eacute;tait arriv&eacute;.</p>

<p><sup class="versenum">11&nbsp;</sup>Comme il ne quittait pas Pierre et Jean, tout le peuple &eacute;tonn&eacute; accourut vers eux, au portique dit de Salomon.</p>

<p><sup class="versenum">12&nbsp;</sup>Pierre, voyant cela, dit au peuple: Hommes Isra&eacute;lites, pourquoi vous &eacute;tonnez-vous de cela? Pourquoi avez-vous les regards fix&eacute;s sur nous, comme si c&#39;&eacute;tait par notre propre puissance ou par notre pi&eacute;t&eacute; que nous eussions fait marcher cet homme?</p>

<p><sup class="versenum">13&nbsp;</sup>Le Dieu d&#39;Abraham, d&#39;Isaac et de Jacob, le Dieu de nos p&egrave;res, a glorifi&eacute; son serviteur J&eacute;sus, que vous avez livr&eacute; et reni&eacute; devant Pilate, qui &eacute;tait d&#39;avis qu&#39;on le rel&acirc;ch&acirc;t.</p>

<p><sup class="versenum">14&nbsp;</sup>Vous avez reni&eacute; le Saint et le Juste, et vous avez demand&eacute; qu&#39;on vous accord&acirc;t la gr&acirc;ce d&#39;un meurtrier.</p>

<p><sup class="versenum">15&nbsp;</sup>Vous avez fait mourir le Prince de la vie, que Dieu a ressuscit&eacute; des morts; nous en sommes t&eacute;moins.</p>

<p><sup class="versenum">16&nbsp;</sup>C&#39;est par la foi en son nom que son nom a raffermi celui que vous voyez et connaissez; c&#39;est la foi en lui qui a donn&eacute; &agrave; cet homme cette enti&egrave;re gu&eacute;rison, en pr&eacute;sence de vous tous.</p>

<p><sup class="versenum">17&nbsp;</sup>Et maintenant, fr&egrave;res, je sais que vous avez agi par ignorance, ainsi que vos chefs.</p>

<p><sup class="versenum">18&nbsp;</sup>Mais Dieu a accompli de la sorte ce qu&#39;il avait annonc&eacute; d&#39;avance par la bouche de tous ses proph&egrave;tes, que son Christ devait souffrir.</p>

<p><sup class="versenum">19&nbsp;</sup>Repentez-vous donc et convertissez-vous, pour que vos p&eacute;ch&eacute;s soient effac&eacute;s,</p>

<p><sup class="versenum">20&nbsp;</sup>afin que des temps de rafra&icirc;chissement viennent de la part du Seigneur, et qu&#39;il envoie celui qui vous a &eacute;t&eacute; destin&eacute;, J&eacute;sus Christ,</p>

<p><sup class="versenum">21&nbsp;</sup>que le ciel doit recevoir jusqu&#39;aux temps du r&eacute;tablissement de toutes choses, dont Dieu a parl&eacute; anciennement par la bouche de ses saints proph&egrave;tes.</p>

<p><sup class="versenum">22&nbsp;</sup>Mo&iuml;se a dit: Le Seigneur votre Dieu vous suscitera d&#39;entre vos fr&egrave;res un proph&egrave;te comme moi; vous l&#39;&eacute;couterez dans tout ce qu&#39;il vous dira,</p>

<p><sup class="versenum">23&nbsp;</sup>et quiconque n&#39;&eacute;coutera pas ce proph&egrave;te sera extermin&eacute; du milieu du peuple.</p>

<p><sup class="versenum">24&nbsp;</sup>Tous les proph&egrave;tes qui ont successivement parl&eacute;, depuis Samuel, ont aussi annonc&eacute; ces jours-l&agrave;.</p>

<p><sup class="versenum">25&nbsp;</sup>Vous &ecirc;tes les fils des proph&egrave;tes et de l&#39;alliance que Dieu a trait&eacute;e avec nos p&egrave;res, en disant &agrave; Abraham: Toutes les familles de la terre seront b&eacute;nies en ta post&eacute;rit&eacute;.</p>

<p><sup class="versenum">26&nbsp;</sup>C&#39;est &agrave; vous premi&egrave;rement que Dieu, ayant suscit&eacute; son serviteur, l&#39;a envoy&eacute; pour vous b&eacute;nir, en d&eacute;tournant chacun de vous de ses iniquit&eacute;s.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/306.mp4" type="button" class="external-movie">
         Regardez Actes 3 </button>
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
	<li class="nobreak-final-final"><span><span>C&#39;est le premier miracle que J&eacute;sus a fait apr&egrave;s son ascension. Les disciples continuaient &agrave; vivre son mod&egrave;le de puissance et de d&eacute;pendance du Saint-Esprit. Pierre et Jean poursuivaient leur routine habituelle lorsque cet &eacute;v&eacute;nement a eu lieu. J&eacute;sus leur avait appris &agrave; donner &agrave; quiconque leur demandait, (<span class="popup-link" @click = "popUp('pop3')"> Matthieu 5:42</span>)&nbsp;</span></span>

	<div class="popup invisible" id="pop3"><span><span><!-- begin bible --> </span></span>

	<p><span><span><sup class="versenum">42&nbsp;</sup>Donne &agrave; celui qui te demande, et ne te d&eacute;tourne pas de celui qui veut emprunter de toi.</span></span></p>
	<span><span> <!-- end bible --> </span></span></div>
	<span><span>&nbsp;et ils avaient d&eacute;j&agrave; fait l&#39;exp&eacute;rience de se laisser utiliser pour gu&eacute;rir les autres au cours de leurs voyages missionnaires &agrave; court terme (<span class="popup-link" @click = "popUp('pop4')"> Matthieu 10</span>).&nbsp;</span></span>

	<div class="popup invisible" id="pop4"><span><span><!-- begin bible --></span></span>

	<div>
	<div>
	<div>
	<div>
	<div>
	<div>
	<p><span><span><sup class="versenum">1 </sup>Puis, ayant appel&eacute; ses douze disciples, il leur donna le pouvoir de chasser les esprits impurs, et de gu&eacute;rir toute maladie et toute infirmit&eacute;.</span></span></p>

	<p><span><span><sup class="versenum">2&nbsp;</sup>Voici les noms des douze ap&ocirc;tres. Le premier, Simon appel&eacute; Pierre, et Andr&eacute;, son fr&egrave;re; Jacques, fils de Z&eacute;b&eacute;d&eacute;e, et Jean, son fr&egrave;re;</span></span></p>

	<p><span><span><sup class="versenum">3&nbsp;</sup>Philippe, et Barth&eacute;lemy; Thomas, et Matthieu, le publicain; Jacques, fils d&#39;Alph&eacute;e, et Thadd&eacute;e;</span></span></p>

	<p><span><span><sup class="versenum">4&nbsp;</sup>Simon le Cananite, et Judas l&#39;Iscariot, celui qui livra J&eacute;sus.</span></span></p>

	<p><span><span><sup class="versenum">5&nbsp;</sup>Tels sont les douze que J&eacute;sus envoya, apr&egrave;s leur avoir donn&eacute; les instructions suivantes: N&#39;allez pas vers les pa&iuml;ens, et n&#39;entrez pas dans les villes des Samaritains;</span></span></p>

	<p><span><span><sup class="versenum">6&nbsp;</sup>allez plut&ocirc;t vers les brebis perdues de la maison d&#39;Isra&euml;l.</span></span></p>

	<p><span><span><sup class="versenum">7&nbsp;</sup>Allez, pr&ecirc;chez, et dites: Le royaume des cieux est proche.</span></span></p>

	<p><span><span><sup class="versenum">8&nbsp;</sup>Gu&eacute;rissez les malades, ressuscitez les morts, purifiez les l&eacute;preux, chassez les d&eacute;mons. Vous avez re&ccedil;u gratuitement, donnez gratuitement.</span></span></p>

	<p><span><span><sup class="versenum">9&nbsp;</sup>Ne prenez ni or, ni argent, ni monnaie, dans vos ceintures;</span></span></p>

	<p><span><span><sup class="versenum">10&nbsp;</sup>ni sac pour le voyage, ni deux tuniques, ni souliers, ni b&acirc;ton; car l&#39;ouvrier m&eacute;rite sa nourriture.</span></span></p>

	<p><span><span><sup class="versenum">11&nbsp;</sup>Dans quelque ville ou village que vous entriez, informez-vous s&#39;il s&#39;y trouve quelque homme digne de vous recevoir; et demeurez chez lui jusqu&#39;&agrave; ce que vous partiez.</span></span></p>

	<p><span><span><sup class="versenum">12&nbsp;</sup>En entrant dans la maison, saluez-la;</span></span></p>

	<p><span><span><sup class="versenum">13&nbsp;</sup>et, si la maison en est digne, que votre paix vienne sur elle; mais si elle n&#39;en est pas digne, que votre paix retourne &agrave; vous.</span></span></p>

	<p><span><span><sup class="versenum">14&nbsp;</sup>Lorsqu&#39;on ne vous recevra pas et qu&#39;on n&#39;&eacute;coutera pas vos paroles, sortez de cette maison ou de cette ville et secouez la poussi&egrave;re de vos pieds.</span></span></p>

	<p><span><span><sup class="versenum">15&nbsp;</sup>Je vous le dis en v&eacute;rit&eacute;: au jour du jugement, le pays de Sodome et de Gomorrhe sera trait&eacute; moins rigoureusement que cette ville-l&agrave;.</span></span></p>

	<p><span><span><sup class="versenum">16&nbsp;</sup>Voici, je vous envoie comme des brebis au milieu des loups. Soyez donc prudents comme les serpents, et simples comme les colombes.</span></span></p>

	<p><span><span><sup class="versenum">17&nbsp;</sup>Mettez-vous en garde contre les hommes; car ils vous livreront aux tribunaux, et ils vous battront de verges dans leurs synagogues;</span></span></p>

	<p><span><span><sup class="versenum">18&nbsp;</sup>vous serez men&eacute;s, &agrave; cause de moi, devant des gouverneurs et devant des rois, pour servir de t&eacute;moignage &agrave; eux et aux pa&iuml;ens.</span></span></p>

	<p><span><span><sup class="versenum">19&nbsp;</sup>Mais, quand on vous livrera, ne vous inqui&eacute;tez ni de la mani&egrave;re dont vous parlerez ni de ce que vous direz: ce que vous aurez &agrave; dire vous sera donn&eacute; &agrave; l&#39;heure m&ecirc;me;</span></span></p>

	<p><span><span><sup class="versenum">20&nbsp;</sup>car ce n&#39;est pas vous qui parlerez, c&#39;est l&#39;Esprit de votre P&egrave;re qui parlera en vous.</span></span></p>

	<p><span><span><sup class="versenum">21&nbsp;</sup>Le fr&egrave;re livrera son fr&egrave;re &agrave; la mort, et le p&egrave;re son enfant; les enfants se soul&egrave;veront contre leurs parents, et les feront mourir.</span></span></p>

	<p><span><span><sup class="versenum">22&nbsp;</sup>Vous serez ha&iuml;s de tous, &agrave; cause de mon nom; mais celui qui pers&eacute;v&eacute;rera jusqu&#39;&agrave; la fin sera sauv&eacute;.</span></span></p>

	<p><span><span><sup class="versenum">23&nbsp;</sup>Quand on vous pers&eacute;cutera dans une ville, fuyez dans une autre. Je vous le dis en v&eacute;rit&eacute;, vous n&#39;aurez pas achev&eacute; de parcourir les villes d&#39;Isra&euml;l que le Fils de l&#39;homme sera venu.</span></span></p>

	<p><span><span><sup class="versenum">24&nbsp;</sup>Le disciple n&#39;est pas plus que le ma&icirc;tre, ni le serviteur plus que son seigneur.</span></span></p>

	<p><span><span><sup class="versenum">25&nbsp;</sup>Il suffit au disciple d&#39;&ecirc;tre trait&eacute; comme son ma&icirc;tre, et au serviteur comme son seigneur. S&#39;ils ont appel&eacute; le ma&icirc;tre de la maison B&eacute;elz&eacute;bul, &agrave; combien plus forte raison appelleront-ils ainsi les gens de sa maison!</span></span></p>

	<p><span><span><sup class="versenum">26&nbsp;</sup>Ne les craignez donc point; car il n&#39;y a rien de cach&eacute; qui ne doive &ecirc;tre d&eacute;couvert, ni de secret qui ne doive &ecirc;tre connu.</span></span></p>

	<p><span><span><sup class="versenum">27&nbsp;</sup>Ce que je vous dis dans les t&eacute;n&egrave;bres, dites-le en plein jour; et ce qui vous est dit &agrave; l&#39;oreille, pr&ecirc;chez-le sur les toits.</span></span></p>

	<p><span><span><sup class="versenum">28&nbsp;</sup>Ne craignez pas ceux qui tuent le corps et qui ne peuvent tuer l&#39;&acirc;me; craignez plut&ocirc;t celui qui peut faire p&eacute;rir l&#39;&acirc;me et le corps dans la g&eacute;henne.</span></span></p>

	<p><span><span><sup class="versenum">29&nbsp;</sup>Ne vend-on pas deux passereaux pour un sou? Cependant, il n&#39;en tombe pas un &agrave; terre sans la volont&eacute; de votre P&egrave;re.</span></span></p>

	<p><span><span><sup class="versenum">30&nbsp;</sup>Et m&ecirc;me les cheveux de votre t&ecirc;te sont tous compt&eacute;s.</span></span></p>

	<p><span><span><sup class="versenum">31&nbsp;</sup>Ne craignez donc point: vous valez plus que beaucoup de passereaux.</span></span></p>

	<p><span><span><sup class="versenum">32&nbsp;</sup>C&#39;est pourquoi, quiconque me confessera devant les hommes, je le confesserai aussi devant mon P&egrave;re qui est dans les cieux;</span></span></p>

	<p><span><span><sup class="versenum">33&nbsp;</sup>mais quiconque me reniera devant les hommes, je le renierai aussi devant mon P&egrave;re qui est dans les cieux.</span></span></p>

	<p><span><span><sup class="versenum">34&nbsp;</sup>Ne croyez pas que je sois venu apporter la paix sur la terre; je ne suis pas venu apporter la paix, mais l&#39;&eacute;p&eacute;e.</span></span></p>

	<p><span><span><sup class="versenum">35&nbsp;</sup>Car je suis venu mettre la division entre l&#39;homme et son p&egrave;re, entre la fille et sa m&egrave;re, entre la belle-fille et sa belle-m&egrave;re;</span></span></p>

	<p><span><span><sup class="versenum">36&nbsp;</sup>et l&#39;homme aura pour ennemis les gens de sa maison.</span></span></p>

	<p><span><span><sup class="versenum">37&nbsp;</sup>Celui qui aime son p&egrave;re ou sa m&egrave;re plus que moi n&#39;est pas digne de moi, et celui qui aime son fils ou sa fille plus que moi n&#39;est pas digne de moi;</span></span></p>

	<p><span><span><sup class="versenum">38&nbsp;</sup>celui qui ne prend pas sa croix, et ne me suit pas, n&#39;est pas digne de moi.</span></span></p>

	<p><span><span><sup class="versenum">39&nbsp;</sup>Celui qui conservera sa vie la perdra, et celui qui perdra sa vie &agrave; cause de moi la retrouvera.</span></span></p>

	<p><span><span><sup class="versenum">40&nbsp;</sup>Celui qui vous re&ccedil;oit me re&ccedil;oit, et celui qui me re&ccedil;oit, re&ccedil;oit celui qui m&#39;a envoy&eacute;.</span></span></p>

	<p><span><span><sup class="versenum">41&nbsp;</sup>Celui qui re&ccedil;oit un proph&egrave;te en qualit&eacute; de proph&egrave;te recevra une r&eacute;compense de proph&egrave;te, et celui qui re&ccedil;oit un juste en qualit&eacute; de juste recevra une r&eacute;compense de juste.</span></span></p>

	<p><span><span><sup class="versenum">42&nbsp;</sup>Et quiconque donnera seulement un verre d&#39;eau froide &agrave; l&#39;un de ces petits parce qu&#39;il est mon disciple, je vous le dis en v&eacute;rit&eacute;, il ne perdra point sa r&eacute;compense.</span></span></p>
	</div>
	</div>
	</div>
	</div>
	</div>
	</div>
	<span><span> <!-- end bible --> </span></span></div>
	<span><span>Pierre a vite soulign&eacute; que la gu&eacute;rison &eacute;tait l&#39;&oelig;uvre de J&eacute;sus ressuscit&eacute;, vivant et pr&eacute;sent. Ce miracle a donn&eacute; &agrave; Pierre et &agrave; Jean l&#39;occasion de t&eacute;moigner devant toutes les personnes pr&eacute;sentes dans les parvis du temple. Nous devons &ecirc;tre pr&ecirc;ts &agrave; ob&eacute;ir aux sollicitations du Saint-Esprit en toute circonstance.</span></span></li>
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

			<td class="social" @click="share('lesson', 'Jésus utilise Pierre et Jean pour guérir un mendiant boiteux: ', '/content/M2/fra/multiply3/multiply306.html')">
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