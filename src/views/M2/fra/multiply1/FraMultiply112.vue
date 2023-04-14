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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply1-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>12.</h1></div>
                        <div class="chapter_title ltr"><h1>Ouvrir des Portes</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="back">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</p>

<ul>
	<li>Exemple: Lisez <span class="popup-link" @click = "popUp('pop1')"> Psaumes 9:1-2</span>&nbsp;&nbsp;et ex&eacute;cutez des chants.

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Au chef des chantres. Sur &laquo;Meurs pour le fils&raquo;. Psaume de David. Je louerai l&#39;&Eacute;ternel de tout mon coeur, Je raconterai toutes tes merveilles.</p>

	<p><sup class="versenum">2&nbsp;</sup>Je ferai de toi le sujet de ma joie et de mon all&eacute;gresse, Je chanterai ton nom, Dieu Tr&egrave;s Haut!</p>
	<!-- end bible --></div>
	</li>
</ul>

</div>

<ul>
</ul>

<h2>Soin</h2>

<p>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la Fid&eacute;lit&eacute;</h2>

<p>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour</p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

<p>Exemple: Puisque tout le monde est appel&eacute; &agrave; suivre J&eacute;sus et &agrave; p&ecirc;cher des hommes, nous devrions r&eacute;aliser qu&#39;il n&#39;y a que deux types de personnes dans le monde: les perdues et les sauv&eacute;es. Les personnes perdues doivent suivre J&eacute;sus. Les personnes sauv&eacute;es doivent apprendre &agrave; p&ecirc;cher les perdues. Lorsque vous voyez le monde comme constitu&eacute; de deux types de personnes, vos interactions quotidiennes deviennent beaucoup plus simples. Si vous rencontrez une personne perdue, t&eacute;moignez-lui. Si vous rencontrez une personne sauv&eacute;e, proposez-lui de la former. C&rsquo;est aussi simple que cela !</p>

</div>
</div>

<div class="up">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><h2>+ Contexte</h2></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<p>Pierre a &eacute;t&eacute; conduit par l&#39;Esprit &agrave; se rendre dans une ville c&ocirc;ti&egrave;re appel&eacute;e C&eacute;sar&eacute;e o&ugrave; vivait un chef militaire romain nomm&eacute; Corneille. Il &eacute;tait un homme de paix pr&eacute;par&eacute; par Dieu. Pierre a ob&eacute;i et s&#39;est rendu &agrave; C&eacute;sar&eacute;e pour parler de J&eacute;sus &agrave; Corneille. Voyons ce qui s&rsquo;est pass&eacute;.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Actes 10:24-48 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 10:24-48</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">24&nbsp;</sup>Ils arriv&egrave;rent &agrave; C&eacute;sar&eacute;e le jour suivant. Corneille les attendait, et avait invit&eacute; ses parents et ses amis intimes.</p>

<p><sup class="versenum">25&nbsp;</sup>Lorsque Pierre entra, Corneille, qui &eacute;tait all&eacute; au-devant de lui, tomba &agrave; ses pieds et se prosterna.</p>

<p><sup class="versenum">26&nbsp;</sup>Mais Pierre le releva, en disant: L&egrave;ve-toi; moi aussi, je suis un homme.</p>

<p><sup class="versenum">27&nbsp;</sup>Et conversant avec lui, il entra, et trouva beaucoup de personnes r&eacute;unies.</p>

<p><sup class="versenum">28&nbsp;</sup>Vous savez, leur dit-il, qu&#39;il est d&eacute;fendu &agrave; un Juif de se lier avec un &eacute;tranger ou d&#39;entrer chez lui; mais Dieu m&#39;a appris &agrave; ne regarder aucun homme comme souill&eacute; et impur.</p>

<p><sup class="versenum">29&nbsp;</sup>C&#39;est pourquoi je n&#39;ai pas eu d&#39;objection &agrave; venir, puisque vous m&#39;avez appel&eacute;; je vous demande donc pour quel motif vous m&#39;avez envoy&eacute; chercher.</p>

<p><sup class="versenum">30&nbsp;</sup>Corneille dit: Il y a quatre jours, &agrave; cette heure-ci, je priais dans ma maison &agrave; la neuvi&egrave;me heure; et voici, un homme v&ecirc;tu d&#39;un habit &eacute;clatant se pr&eacute;senta devant moi, et dit:</p>

<p><sup class="versenum">31&nbsp;</sup>Corneille, ta pri&egrave;re a &eacute;t&eacute; exauc&eacute;e, et Dieu s&#39;est souvenu de tes aum&ocirc;nes.</p>

<p><sup class="versenum">32&nbsp;</sup>Envoie donc &agrave; Jopp&eacute;, et fais venir Simon, surnomm&eacute; Pierre; il est log&eacute; dans la maison de Simon, corroyeur, pr&egrave;s de la mer.</p>

<p><sup class="versenum">33&nbsp;</sup>Aussit&ocirc;t j&#39;ai envoy&eacute; vers toi, et tu as bien fait de venir. Maintenant donc nous sommes tous devant Dieu, pour entendre tout ce que le Seigneur t&#39;a ordonn&eacute; de nous dire.</p>

<p><sup class="versenum">34&nbsp;</sup>Alors Pierre, ouvrant la bouche, dit: En v&eacute;rit&eacute;, je reconnais que Dieu ne fait point acception de personnes,</p>

<p><sup class="versenum">35&nbsp;</sup>mais qu&#39;en toute nation celui qui le craint et qui pratique la justice lui est agr&eacute;able.</p>

<p><sup class="versenum">36&nbsp;</sup>Il a envoy&eacute; la parole aux fils d&#39;Isra&euml;l, en leur annon&ccedil;ant la paix par J&eacute;sus Christ, qui est le Seigneur de tous.</p>

<p><sup class="versenum">37&nbsp;</sup>Vous savez ce qui est arriv&eacute; dans toute la Jud&eacute;e, apr&egrave;s avoir commenc&eacute; en Galil&eacute;e, &agrave; la suite du bapt&ecirc;me que Jean a pr&ecirc;ch&eacute;;</p>

<p><sup class="versenum">38&nbsp;</sup>vous savez comment Dieu a oint du Saint Esprit et de force J&eacute;sus de Nazareth, qui allait de lieu en lieu faisant du bien et gu&eacute;rissant tous ceux qui &eacute;taient sous l&#39;empire du diable, car Dieu &eacute;tait avec lui.</p>

<p><sup class="versenum">39&nbsp;</sup>Nous sommes t&eacute;moins de tout ce qu&#39;il a fait dans le pays des Juifs et &agrave; J&eacute;rusalem. Ils l&#39;ont tu&eacute;, en le pendant au bois.</p>

<p><sup class="versenum">40&nbsp;</sup>Dieu l&#39;a ressuscit&eacute; le troisi&egrave;me jour, et il a permis qu&#39;il appar&ucirc;t,</p>

<p><sup class="versenum">41&nbsp;</sup>non &agrave; tout le peuple, mais aux t&eacute;moins choisis d&#39;avance par Dieu, &agrave; nous qui avons mang&eacute; et bu avec lui, apr&egrave;s qu&#39;il fut ressuscit&eacute; des morts.</p>

<p><sup class="versenum">42&nbsp;</sup>Et J&eacute;sus nous a ordonn&eacute; de pr&ecirc;cher au peuple et d&#39;attester que c&#39;est lui qui a &eacute;t&eacute; &eacute;tabli par Dieu juge des vivants et des morts.</p>

<p><sup class="versenum">43&nbsp;</sup>Tous les proph&egrave;tes rendent de lui le t&eacute;moignage que quiconque croit en lui re&ccedil;oit par son nom le pardon des p&eacute;ch&eacute;s.</p>

<p><sup class="versenum">44&nbsp;</sup>Comme Pierre pronon&ccedil;ait encore ces mots, le Saint Esprit descendit sur tous ceux qui &eacute;coutaient la parole.</p>

<p><sup class="versenum">45&nbsp;</sup>Tous les fid&egrave;les circoncis qui &eacute;taient venus avec Pierre furent &eacute;tonn&eacute;s de ce que le don du Saint Esprit &eacute;tait aussi r&eacute;pandu sur les pa&iuml;ens.</p>

<p><sup class="versenum">46&nbsp;</sup>Car ils les entendaient parler en langues et glorifier Dieu.</p>

<p><sup class="versenum">47&nbsp;</sup>Alors Pierre dit: Peut-on refuser l&#39;eau du bapt&ecirc;me &agrave; ceux qui ont re&ccedil;u le Saint Esprit aussi bien que nous?</p>

<p><sup class="versenum">48&nbsp;</sup>Et il ordonna qu&#39;ils fussent baptis&eacute;s au nom du Seigneur. Sur quoi ils le pri&egrave;rent de rester quelques jours aupr&egrave;s d&#39;eux.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/112.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 10:24-48&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de D&eacute;couverte</h2>

<ul>
	<li>Chacun dit ce qui a retenu son attention (ou ce qu&rsquo;il a aim&eacute; le plus) et pourquoi.</li>
	<li>Pourquoi pensez-vous que cette histoire est importante?</li>
	<li>Comment pouvons-nous vivre diff&eacute;remment maintenant que nous connaissons cette histoire (passage)?</li>
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


<h2>Lire, raconter et corriger</h2>

<ul>
	<li>Relisez l&rsquo;histoire. D&eacute;signez quelqu&rsquo;un pour raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<ul>
	<li class="nobreak-final-final">Les hommes de paix sont des personnes de relation. Nous pouvons partager l&#39;&Eacute;vangile avec des individus, mais nous devons aussi chercher des occasions de suivre des portes ouvertes pour partager avec les amis et la famille des hommes de paix. Lydie et sa famille (<span class="popup-link" @click = "popUp('pop2')"> Actes 16: 14-15</span>).

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">14&nbsp;</sup>L&#39;une d&#39;elles, nomm&eacute;e Lydie, marchande de pourpre, de la ville de Thyatire, &eacute;tait une femme craignant Dieu, et elle &eacute;coutait. Le Seigneur lui ouvrit le coeur, pour qu&#39;elle f&ucirc;t attentive &agrave; ce que disait Paul.</p>

	<p><sup class="versenum">15&nbsp;</sup>Lorsqu&#39;elle eut &eacute;t&eacute; baptis&eacute;e, avec sa famille, elle nous fit cette demande: Si vous me jugez fid&egrave;le au Seigneur, entrez dans ma maison, et demeurez-y. Et elle nous pressa par ses instances.</p>
	<!-- end bible --></div>
	&nbsp;le ge&ocirc;lier de Philippes et sa famille (<span class="popup-link" @click = "popUp('pop3')"> Actes 16: 30-33</span>)&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">30&nbsp;</sup>il les fit sortir, et dit: Seigneurs, que faut-il que je fasse pour &ecirc;tre sauv&eacute;?</p>

	<p><sup class="versenum">31&nbsp;</sup>Paul et Silas r&eacute;pondirent: Crois au Seigneur J&eacute;sus, et tu seras sauv&eacute;, toi et ta famille.</p>

	<p><sup class="versenum">32&nbsp;</sup>Et ils lui annonc&egrave;rent la parole du Seigneur, ainsi qu&#39;&agrave; tous ceux qui &eacute;taient dans sa maison.</p>

	<p><sup class="versenum">33&nbsp;</sup>Il les prit avec lui, &agrave; cette heure m&ecirc;me de la nuit, il lava leurs plaies, et aussit&ocirc;t il fut baptis&eacute;, lui et tous les siens.</p>
	<!-- end bible --></div>
	et Matthieu le collecteur d&rsquo;imp&ocirc;t et ses amis (<span class="popup-link" @click = "popUp('pop4')"> Matthieu 9: 9-10</span>)&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">9&nbsp;</sup>De l&agrave; &eacute;tant all&eacute; plus loin, J&eacute;sus vit un homme assis au lieu des p&eacute;ages, et qui s&#39;appelait Matthieu. Il lui dit: Suis-moi. Cet homme se leva, et le suivit.</p>

	<p><sup class="versenum">10&nbsp;</sup>Comme J&eacute;sus &eacute;tait &agrave; table dans la maison, voici, beaucoup de publicains et de gens de mauvaise vie vinrent se mettre &agrave; table avec lui et avec ses disciples.</p>
	<!-- end bible --></div>
	sont d&#39;autres exemples de l&#39;&eacute;vangile qui se r&eacute;pand dans les relations.</li>
</ul>

</div>
</div>

<div class="forward">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary4" class="summary"><h2>+ Se Pr&eacute;parer pour la Mission</h2></div>
<div class="collapsed" id ="Text4">
<!-- end default revealSummary -->

<p>Appliquez-vous &agrave; organiser un &eacute;v&eacute;nement missionnaire dans la maison d&rsquo;un homme de paix.</p>

<ul>
	<li>Discutez de la fa&ccedil;on dont ils demanderont &agrave; l&rsquo;homme de paix d&rsquo;accueillir l&rsquo;&eacute;v&eacute;nement.</li>
	<li>Discutez de la fa&ccedil;on d&#39;utiliser les courts m&eacute;trages et les extraits du film JESUS pour avoir des discussions spirituelles en utilisant les 2 questions standard.</li>
	<li>Discutez de comment cr&eacute;er une occasion pour la pri&egrave;re.</li>
	<li>Discutez de la fa&ccedil;on dont vous suivrez ceux qui croient en Christ.</li>
</ul>

</div>

<h2>Aller en Mission&nbsp;</h2>

<ul>
	<li>Identifiez au moins un homme de paix &agrave; qui vous pourriez demander d&rsquo;accueillir un &eacute;v&eacute;nement.</li>
	<li>Identifiez 5 personnes de votre Liste de R&eacute;seau envers qui vous prendrez l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>&Eacute;crivez les promesses &laquo; je le ferai d&rsquo;ici quand &raquo; et parlez-en &agrave; votre groupe.</li>
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


<h2>Prier pour la Mission</h2>

<p>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples.</p>
</div>

<div class="for-enrichment">Pour en savoir davantage veuillez lire le <!-- begin linkInternal capacitor-->
<span id= "Return1" class="internal-link" @click="this.goToPageAndSetReturn('/M2/fra/tc/ct07', '#1')">
    Message transmissible N&deg; 7 : Comment aider &agrave; accomplir la Grande Commission 
</span>
<!-- end linkInternal capacitor-->
 et en discuter avec un autre membre du groupe.</div>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Ouvrir des Portes: ', '/content/M2/fra/multiply1/multiply112.html')">
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