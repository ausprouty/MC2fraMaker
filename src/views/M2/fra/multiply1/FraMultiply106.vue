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
                        <div class="chapter_number ltr"><h1>6.</h1></div>
                        <div class="chapter_title ltr"><h1>Parler avec Dieu</h1></div>
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

<p>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration</p>

<ul>
	<li>Exemple: Lisez <span class="popup-link" @click = "popUp('pop1')"> Psaumes 100:2</span>

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">2&nbsp;</sup>Servez l&#39;&Eacute;ternel, avec joie, Venez avec all&eacute;gresse en sa pr&eacute;sence!</p>
	<!-- end bible --></div>
	&laquo; Servez l&rsquo;Eternel, avec joie, Venez avec all&eacute;gresse en sa pr&eacute;sence! &raquo; Apprenons une chanson que nous pouvons ex&eacute;cuter pour louer le Seigneur.</li>
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

<p>Exemple: Lorsque J&eacute;sus parcourait villes et villages, il vit le besoin des gens, et fut &eacute;pris de compassion &agrave; leur &eacute;gard. Il dit &agrave; ses disciples, &laquo; La moisson est grande mais il y a peu d&rsquo;ouvriers. Priez donc le ma&icirc;tre de la moisson d&rsquo;envoyer des ouvriers dans sa moisson. &raquo; Dieu veut que tout le monde le connaisse ainsi que son amour. Il veut nous utiliser et il suscitera plus d&rsquo;ouvriers &agrave; partir de la moisson que nous r&eacute;colteront. Continuons &agrave; demander &agrave; Dieu d&rsquo;envoyer plus d&rsquo;ouvriers pour amener les hommes &agrave; le connaitre.</p>

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

<p>Quand bien m&ecirc;me J&eacute;sus s&rsquo;&eacute;tait affair&eacute; &agrave; accomplir la mission, il passait beaucoup de temps &agrave; parler au P&egrave;re. Etant donn&eacute; que ses disciples le regardaient, ils voudraient eux-aussi apprendre &agrave; parler au P&egrave;re. Aujourd&rsquo;hui, nous allons apprendre ce qu&rsquo;ils ont dit au p&egrave;re.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Luc 11:1-13 deux fois pendant que tout le monde &eacute;coute.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 11:1-13</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>J&eacute;sus priait un jour en un certain lieu. Lorsqu&#39;il eut achev&eacute;, un de ses disciples lui dit: Seigneur, enseigne-nous &agrave; prier, comme Jean l&#39;a enseign&eacute; &agrave; ses disciples.</p>

<p><sup class="versenum">2&nbsp;</sup>Il leur dit: Quand vous priez, dites: P&egrave;re! Que ton nom soit sanctifi&eacute;; que ton r&egrave;gne vienne.</p>

<p><sup class="versenum">3&nbsp;</sup>Donne-nous chaque jour notre pain quotidien;</p>

<p><sup class="versenum">4&nbsp;</sup>pardonne-nous nos p&eacute;ch&eacute;s, car nous aussi nous pardonnons &agrave; quiconque nous offense; et ne nous induis pas en tentation.</p>

<p><sup class="versenum">5&nbsp;</sup>Il leur dit encore: Si l&#39;un de vous a un ami, et qu&#39;il aille le trouver au milieu de la nuit pour lui dire: Ami, pr&ecirc;te-moi trois pains,</p>

<p><sup class="versenum">6&nbsp;</sup>car un de mes amis est arriv&eacute; de voyage chez moi, et je n&#39;ai rien &agrave; lui offrir,</p>

<p><sup class="versenum">7&nbsp;</sup>et si, de l&#39;int&eacute;rieur de sa maison, cet ami lui r&eacute;pond: Ne m&#39;importune pas, la porte est d&eacute;j&agrave; ferm&eacute;e, mes enfants et moi sommes au lit, je ne puis me lever pour te donner des pains, -</p>

<p><sup class="versenum">8&nbsp;</sup>je vous le dis, m&ecirc;me s&#39;il ne se levait pas pour les lui donner parce que c&#39;est son ami, il se l&egrave;verait &agrave; cause de son importunit&eacute; et lui donnerait tout ce dont il a besoin.</p>

<p><sup class="versenum">9&nbsp;</sup>Et moi, je vous dis: Demandez, et l&#39;on vous donnera; cherchez, et vous trouverez; frappez, et l&#39;on vous ouvrira.</p>

<p><sup class="versenum">10&nbsp;</sup>Car quiconque demande re&ccedil;oit, celui qui cherche trouve, et l&#39;on ouvre &agrave; celui qui frappe.</p>

<p><sup class="versenum">11&nbsp;</sup>Quel est parmi vous le p&egrave;re qui donnera une pierre &agrave; son fils, s&#39;il lui demande du pain? Ou, s&#39;il demande un poisson, lui donnera-t-il un serpent au lieu d&#39;un poisson?</p>

<p><sup class="versenum">12&nbsp;</sup>Ou, s&#39;il demande un oeuf, lui donnera-t-il un scorpion?</p>

<p><sup class="versenum">13&nbsp;</sup>Si donc, m&eacute;chants comme vous l&#39;&ecirc;tes, vous savez donner de bonnes choses &agrave; vos enfants, &agrave; combien plus forte raison le P&egrave;re c&eacute;leste donnera-t-il le Saint Esprit &agrave; ceux qui le lui demandent.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/106.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 11:1-13&nbsp; </button>
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

<p>La pri&egrave;re consiste simplement &agrave; parler &agrave; notre P&egrave;re qui est dans les cieux. Nous pouvons r&eacute;sumer l&rsquo;enseignement de J&eacute;sus en 4 points que sont:</p>

<ul>
	<li>Louez-le et faites de Lui le centre (de votre vie);</li>
	<li>Lui demander ce que vous voulez;</li>
	<li>Reconnaitre vos p&eacute;ch&eacute;s;</li>
	<li>Soumettre votre vie &agrave; sa volont&eacute;, et &agrave; son royaume.</li>
</ul>

<p>Nous pouvons avoir la certitude qu&rsquo;il nous a exauc&eacute;s et que son c&oelig;ur ne peut nous donner que ce qui est bon.</p>

<p>Pour une &eacute;tude plus approfondie: Lisez le Message Transmissible #9: Comment prier puis discutez avec un autre membre du groupe.</p>

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
	<li>Prier en utilisant les 4 points du r&eacute;sum&eacute;</li>
	<li>Partager l&rsquo;Evangile &agrave; propos du Saint-Esprit, l&rsquo;&eacute;tude de la bible ou &agrave; propos de n&rsquo;importe quelle autre le&ccedil;on pass&eacute;e</li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission&nbsp;</h2>

<ul>
	<li>Identifiez 5 personnes de votre liste de r&eacute;seau, &agrave; qui vous raconterez l&rsquo;histoire ou annoncerez la bonne nouvelle cette semaine.</li>
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

<ul>
	<li>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples.</li>
</ul>
</div>

<div class="for-enrichment">Pour en savoir davantage veuillez lire le <!-- begin linkInternal capacitor-->
<span id= "Return1" class="internal-link" @click="this.goToPageAndSetReturn('/M2/fra/tc/ct09', '#1')">
    Message transmissible N&deg; 9 : Comment prier 
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

			<td class="social" @click="share('lesson', 'Parler avec Dieu: ', '/content/M2/fra/multiply1/multiply106.html')">
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