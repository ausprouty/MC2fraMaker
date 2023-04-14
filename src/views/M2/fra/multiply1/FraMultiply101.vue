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
                        <div class="chapter_number ltr"><h1>1.</h1></div>
                        <div class="chapter_title ltr"><h1>Assurance du Salut</h1></div>
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
	<li>Lisez <span class="popup-link" @click = "popUp('pop1')"> Psaumes 118:28</span>

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">28&nbsp;</sup>Tu es mon Dieu, et je te louerai; Mon Dieu! je t&#39;exalterai.</p>
	<!-- end bible --></div>
	&laquo; Tu es mon Dieu, et je te louerai ; Mon Dieu! je t&rsquo;exalterai. &raquo; Pour quoi pouvons-nous remercier et louer Dieu aujourd&rsquo;hui?</li>
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
	<li class="nobreak-final-final">Exemple: Dieu aime les hommes! La Bible nous dit que le d&eacute;sir de Dieu est que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;. (<span class="popup-link" @click = "popUp('pop2')"> 1 Timoth&eacute;e 2:4</span>).&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">4&nbsp;</sup>qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;.</p>
	<!-- end bible --></div>
	&nbsp;L&rsquo;&eacute;vangile n&rsquo;est pas pour vous seuls mais pour tous vos amis et famille. Dieu les aime et va vous utiliser pour leur transmettre ce que vous apprenez au sujet de J&eacute;sus pour qu&rsquo;ils puissent aussi suivre J&eacute;sus. Puisque nous voyageons ensemble, il serait passionnant de voir ce que Dieu fera dans la vie de ceux qui nous entourent.</li>
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

<p>J&eacute;sus enseignait qu&rsquo;Il est le bon berger qui donne sa vie pour ses brebis (v 11). Il a aussi dit, &laquo; Je connais mes brebis et elles me connaissent, &raquo; et &laquo; Je suis venu afin que les brebis aient la vie et qu&rsquo;elles soient dans l&rsquo;abondance. &raquo; cependant, beaucoup de Juifs ne Le croient pas, et doutent de Ses d&eacute;clarations. C&rsquo;est l&agrave; o&ugrave; notre histoire commence.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Jean 10:22-30 deux fois pendant que tout le monde &eacute;coute</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 10:22-30</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">22&nbsp;</sup>On c&eacute;l&eacute;brait &agrave; J&eacute;rusalem la f&ecirc;te de la D&eacute;dicace. C&#39;&eacute;tait l&#39;hiver.</p>

<p><sup class="versenum">23&nbsp;</sup>Et J&eacute;sus se promenait dans le temple, sous le portique de Salomon.</p>

<p><sup class="versenum">24&nbsp;</sup>Les Juifs l&#39;entour&egrave;rent, et lui dirent: Jusques &agrave; quand tiendras-tu notre esprit en suspens? Si tu es le Christ, dis-le nous franchement.</p>

<p><sup class="versenum">25&nbsp;</sup>J&eacute;sus leur r&eacute;pondit: Je vous l&#39;ai dit, et vous ne croyez pas. Les oeuvres que je fais au nom de mon P&egrave;re rendent t&eacute;moignage de moi.</p>

<p><sup class="versenum">26&nbsp;</sup>Mais vous ne croyez pas, parce que vous n&#39;&ecirc;tes pas de mes brebis.</p>

<p><sup class="versenum">27&nbsp;</sup>Mes brebis entendent ma voix; je les connais, et elles me suivent.</p>

<p><sup class="versenum">28&nbsp;</sup>Je leur donne la vie &eacute;ternelle; et elles ne p&eacute;riront jamais, et personne ne les ravira de ma main.</p>

<p><sup class="versenum">29&nbsp;</sup>Mon P&egrave;re, qui me les a donn&eacute;es, est plus grand que tous; et personne ne peut les ravir de la main de mon P&egrave;re.</p>

<p><sup class="versenum">30&nbsp;</sup>Moi et le P&egrave;re nous sommes un.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/101.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 10:22-30&nbsp; </button>
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

<p>Sur la croix, J&eacute;sus, le bon berger a donn&eacute; Sa vie comme sacrifice pour vos p&eacute;ch&eacute;s. Comme l&#39;une de ses brebis, il veut que vous sachiez que vous avez la vie &eacute;ternelle et que vous ne p&eacute;rirez jamais. Vous &ecirc;tes en s&eacute;curit&eacute; dans ses mains et personne, y compris Satan lui-m&ecirc;me, ne peut vous arracher. Lisez la section assurance de la brochure de l&rsquo;&eacute;vangile.</p>

<p>Pour une &eacute;tude plus approfondi&nbsp;: Lisez le <!-- begin linkInternal capacitor-->
<span id= "Return1" class="internal-link" @click="this.goToPageAndSetReturn('/M2/fra/tc/ct01', '#1')">
    Message transmissible N&deg; 1 : Comment etre surs que vous etes un chretien 
</span>
<!-- end linkInternal capacitor-->
 et discutez avec un autre membre du groupe.</p>

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
	<li>Pratiquez le partage de l&rsquo;&eacute;vangile</li>
	<li>Rappelez-les ce qu&rsquo;il faut faire lorsque quelqu&rsquo;un dit OUI &agrave; l&rsquo;&eacute;vangile.</li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission&nbsp;</h2>

<ul>
	<li>Cr&eacute;ez une Liste de R&eacute;seau en &eacute;crivant le nom de 10 ou plus de personnes que vous connaissez.</li>
	<li>Identifiez 5 personnes de votre Liste de R&eacute;seau &agrave; qui vous raconterez l&rsquo;histoire ou avec qui vous partagerez l&rsquo;&eacute;vangile cette semaine.</li>
	<li>Ecrivez des promesses &laquo; Je le ferai d&rsquo;ici quand &raquo; et dites les &agrave; votre groupe.</li>
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
	<li>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser pour initier un mouvement de faiseurs de disciples.</li>
</ul>
</div>

<div class="for-enrichment">Pour en savoir davantage veuillez lire le <!-- begin linkInternal capacitor-->
<span id= "Return2" class="internal-link" @click="this.goToPageAndSetReturn('/M2/fra/tc/ct01', '#2')">
    Message transmissible N&deg; 1 : Comment etre surs que vous etes un chretien 
</span>
<!-- end linkInternal capacitor-->
 et en discuter avec un autre membre du groupe.&nbsp;</div>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Assurance du Salut: ', '/content/M2/fra/multiply1/multiply101.html')">
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