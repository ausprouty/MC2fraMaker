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
                        <div class="chapter_number ltr"><h1>2.</h1></div>
                        <div class="chapter_title ltr"><h1>Relation et Communion</h1></div>
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

<p>Lisez un passage biblique pour commencer &agrave; poser les fondements de l&#39;adoration et de la louange.</p>

<ul>
	<li>Exemple: <span class="popup-link" @click = "popUp('pop1')"> Psaumes 48:9</span>

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">9&nbsp;</sup>(48:10) O Dieu, nous pensons &agrave; ta bont&eacute; Au milieu de ton temple.</p>
	<!-- end bible --></div>
	&laquo; O Dieu, nous pensons &agrave; ta bont&eacute; Au milieu de ton temple. &raquo; Faisons une pause et disons &agrave; J&eacute;sus combien nous sommes reconnaissants pour Son amour pour nous.</li>
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

<p>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</p>

<ul>
	<li>Demandez, &laquo; Avez-vous pu parler &agrave; quelqu&#39;un de votre d&eacute;cision de suivre Christ? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

<ul>
	<li class="nobreak-final-final">Exemple: lorsque nous acceptons Christ notre vie change pour toujours. <span class="popup-link" @click = "popUp('pop2')"> 2 Corinthiens 5:17</span>

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">17&nbsp;</sup>Si quelqu&#39;un est en Christ, il est une nouvelle cr&eacute;ature. Les choses anciennes sont pass&eacute;es; voici, toutes choses sont devenues nouvelles.</p>
	<!-- end bible --></div>
	dit: Si quelqu&rsquo;un est en Christ, il est une nouvelle cr&eacute;ature. Les choses anciennes sont pass&eacute;es ; voici, toutes choses sont devenues nouvelles! C&rsquo;est nous! Nous sommes une nouvelle cr&eacute;ature et puisque nous suivons Christ, nos vies continueront par changer, pleines d&rsquo;objectifs et de sens. Encourageons-nous les uns les autres avec cette v&eacute;rit&eacute; en continuant notre voyage ensemble dans cette nouvelle vie.</li>
</ul>

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

<p>Ceux qui ne sont pas consid&eacute;r&eacute;s dans la soci&eacute;t&eacute; r&eacute;pondaient favorablement &agrave; l&rsquo;enseignement de J&eacute;sus. Les leaders religieux (Pharisiens) et les docteurs de la loi n&rsquo;ont pas voulu que J&eacute;sus s&rsquo;associe &agrave; ces gens. J&eacute;sus a donc racont&eacute; une histoire au sujet du fils prodigue pour expliquer le c&oelig;ur de Dieu envers les p&eacute;cheurs.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Luc 15:11-24 deux fois pendant que tout le monde &eacute;coute.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 15:11-24</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">11&nbsp;</sup>Il dit encore: Un homme avait deux fils.</p>

<p><sup class="versenum">12&nbsp;</sup>Le plus jeune dit &agrave; son p&egrave;re: Mon p&egrave;re, donne-moi la part de bien qui doit me revenir. Et le p&egrave;re leur partagea son bien.</p>

<p><sup class="versenum">13&nbsp;</sup>Peu de jours apr&egrave;s, le plus jeune fils, ayant tout ramass&eacute;, partit pour un pays &eacute;loign&eacute;, o&ugrave; il dissipa son bien en vivant dans la d&eacute;bauche.</p>

<p><sup class="versenum">14&nbsp;</sup>Lorsqu&#39;il eut tout d&eacute;pens&eacute;, une grande famine survint dans ce pays, et il commen&ccedil;a &agrave; se trouver dans le besoin.</p>

<p><sup class="versenum">15&nbsp;</sup>Il alla se mettre au service d&#39;un des habitants du pays, qui l&#39;envoya dans ses champs garder les pourceaux.</p>

<p><sup class="versenum">16&nbsp;</sup>Il aurait bien voulu se rassasier des carouges que mangeaient les pourceaux, mais personne ne lui en donnait.</p>

<p><sup class="versenum">17&nbsp;</sup>&Eacute;tant rentr&eacute; en lui-m&ecirc;me, il se dit: Combien de mercenaires chez mon p&egrave;re ont du pain en abondance, et moi, ici, je meurs de faim!</p>

<p><sup class="versenum">18&nbsp;</sup>Je me l&egrave;verai, j&#39;irai vers mon p&egrave;re, et je lui dirai: Mon p&egrave;re, j&#39;ai p&eacute;ch&eacute; contre le ciel et contre toi,</p>

<p><sup class="versenum">19&nbsp;</sup>je ne suis plus digne d&#39;&ecirc;tre appel&eacute; ton fils; traite-moi comme l&#39;un de tes mercenaires.</p>

<p><sup class="versenum">20&nbsp;</sup>Et il se leva, et alla vers son p&egrave;re. Comme il &eacute;tait encore loin, son p&egrave;re le vit et fut &eacute;mu de compassion, il courut se jeter &agrave; son cou et le baisa.</p>

<p><sup class="versenum">21&nbsp;</sup>Le fils lui dit: Mon p&egrave;re, j&#39;ai p&eacute;ch&eacute; contre le ciel et contre toi, je ne suis plus digne d&#39;&ecirc;tre appel&eacute; ton fils.</p>

<p><sup class="versenum">22&nbsp;</sup>Mais le p&egrave;re dit &agrave; ses serviteurs: Apportez vite la plus belle robe, et l&#39;en rev&ecirc;tez; mettez-lui un anneau au doigt, et des souliers aux pieds.</p>

<p><sup class="versenum">23&nbsp;</sup>Amenez le veau gras, et tuez-le. Mangeons et r&eacute;jouissons-nous;</p>

<p><sup class="versenum">24&nbsp;</sup>car mon fils que voici &eacute;tait mort, et il est revenu &agrave; la vie; il &eacute;tait perdu, et il est retrouv&eacute;. Et ils commenc&egrave;rent &agrave; se r&eacute;jouir.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/102.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 15:11-24&nbsp; </button>
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
	<li>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<ul>
	<li class="nobreak-final-final">Notre P&egrave;re c&eacute;leste souhaite pardonner les p&eacute;ch&eacute;s de Ses enfants. Notre p&eacute;ch&eacute; ne change pas le fait que Dieu soit notre P&egrave;re. Mais le p&eacute;ch&eacute; a des cons&eacute;quences et affecte bien s&ucirc;r notre communion avec Dieu. Nous ne jouissons pas de notre P&egrave;re. <span class="popup-link" @click = "popUp('pop3')"> 1 Jean 1:9</span>

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">9&nbsp;</sup>Si nous confessons nos p&eacute;ch&eacute;s, il est fid&egrave;le et juste pour nous les pardonner, et pour nous purifier de toute iniquit&eacute;.</p>
	<!-- end bible --></div>
	nous rassure: &laquo; Si nous confessons nos p&eacute;ch&eacute;s, il est fid&egrave;le et juste pour nous les pardonner, et pour nous purifier de toute iniquit&eacute;. &raquo;</li>
</ul>

<p>Pour une &eacute;tude plus approfondie: Lisez le Message transmissible #2: Comment vous pouvez vivre l&rsquo;amour et le pardon de Dieu et discutez avec un autre membre du groupe.</p>

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

<ul>
	<li>R&eacute;visez la Liste de R&eacute;seau et ajouter des gens si n&eacute;cessaire</li>
	<li>Pratiquez le partage de l&rsquo;&eacute;vangile et amenez quelqu&rsquo;un &agrave; prier pour recevoir Christ</li>
	<li>Rappelez-leur ce qu&rsquo;il faut faire lorsque quelqu&rsquo;un dit OUI &agrave; l&rsquo;&eacute;vangile.</li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission&nbsp;</h2>

<ul>
	<li>Identifiez 5 personnes de votre Liste de R&eacute;seau &agrave; qui vous raconterez l&rsquo;histoire ou avec qui vous partagerez l&rsquo;&eacute;vangile cette semaine.</li>
	<li>Ecrivez des promesses &laquo; Je le ferai d&rsquo;ici quand &raquo; et parlez-en &agrave; votre petit groupe.</li>
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

<ul>
	<li>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples.</li>
</ul>
</div>

<div class="for-enrichment">Pour en savoir davantage veuillez lire le <!-- begin linkInternal capacitor-->
<span id= "Return1" class="internal-link" @click="this.goToPageAndSetReturn('/M2/fra/tc/ct02', '#1')">
    Message transmissible N&deg; 2 : L&#39;amour et le pardon de Dieu 
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

			<td class="social" @click="share('lesson', 'Relation et Communion: ', '/content/M2/fra/multiply1/multiply102.html')">
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