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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply2-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>12.</h1></div>
                        <div class="chapter_title ltr"><h1>La source de la Vraie Joie</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</p>

</div>

<h2>Soin</h2>

<p>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la Fid&eacute;lit&eacute;</h2>

<p>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Jean 3:22-35 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 3:22-35</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">22&nbsp;</sup>Apr&egrave;s cela, J&eacute;sus, accompagn&eacute; de ses disciples, se rendit dans la terre de Jud&eacute;e; et l&agrave; il demeurait avec eux, et il baptisait.</p>

<p><sup class="versenum">23&nbsp;</sup>Jean aussi baptisait &agrave; &Eacute;non, pr&egrave;s de Salim, parce qu&#39;il y avait l&agrave; beaucoup d&#39;eau; et on y venait pour &ecirc;tre baptis&eacute;.</p>

<p><sup class="versenum">24&nbsp;</sup>Car Jean n&#39;avait pas encore &eacute;t&eacute; mis en prison.</p>

<p><sup class="versenum">25&nbsp;</sup>Or, il s&#39;&eacute;leva de la part des disciples de Jean une dispute avec un Juif touchant la purification.</p>

<p><sup class="versenum">26&nbsp;</sup>Ils vinrent trouver Jean, et lui dirent: Rabbi, celui qui &eacute;tait avec toi au del&agrave; du Jourdain, et &agrave; qui tu as rendu t&eacute;moignage, voici, il baptise, et tous vont &agrave; lui.</p>

<p><sup class="versenum">27&nbsp;</sup>Jean r&eacute;pondit: Un homme ne peut recevoir que ce qui lui a &eacute;t&eacute; donn&eacute; du ciel.</p>

<p><sup class="versenum">28&nbsp;</sup>Vous-m&ecirc;mes m&#39;&ecirc;tes t&eacute;moins que j&#39;ai dit: Je ne suis pas le Christ, mais j&#39;ai &eacute;t&eacute; envoy&eacute; devant lui.</p>

<p><sup class="versenum">29&nbsp;</sup>Celui &agrave; qui appartient l&#39;&eacute;pouse, c&#39;est l&#39;&eacute;poux; mais l&#39;ami de l&#39;&eacute;poux, qui se tient l&agrave; et qui l&#39;entend, &eacute;prouve une grande joie &agrave; cause de la voix de l&#39;&eacute;poux: aussi cette joie, qui est la mienne, est parfaite.</p>

<p><sup class="versenum">30&nbsp;</sup>Il faut qu&#39;il croisse, et que je diminue.</p>

<p><sup class="versenum">31&nbsp;</sup>Celui qui vient d&#39;en haut est au-dessus de tous; celui qui est de la terre est de la terre, et il parle comme &eacute;tant de la terre. Celui qui vient du ciel est au-dessus de tous,</p>

<p><sup class="versenum">32&nbsp;</sup>il rend t&eacute;moignage de ce qu&#39;il a vu et entendu, et personne ne re&ccedil;oit son t&eacute;moignage.</p>

<p><sup class="versenum">33&nbsp;</sup>Celui qui a re&ccedil;u son t&eacute;moignage a certifi&eacute; que Dieu est vrai;</p>

<p><sup class="versenum">34&nbsp;</sup>car celui que Dieu a envoy&eacute; dit les paroles de Dieu, parce que Dieu ne lui donne pas l&#39;Esprit avec mesure.</p>

<p><sup class="versenum">35&nbsp;</sup>Le P&egrave;re aime le Fils, et il a remis toutes choses entre ses mains.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/212.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 3:22-35&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de D&eacute;couverte</h2>

<p>Etudiez chaque passage en utilisant les questions de discussion suivantes:</p>

<ul>
	<li>Qu&rsquo;est-ce qui a retenu votre attention ou qu&rsquo;avez-vous aim&eacute; le plus ?</li>
	<li>Qu&rsquo;est ce qui est nouveau ou s&rsquo;est d&eacute;velopp&eacute; &agrave; ce point de l&rsquo;histoire de J&eacute;sus?</li>
	<li>Quelle implication du point de vue de l&rsquo;humanit&eacute; ou de la divinit&eacute; de J&eacute;sus voyez-vous dans ce passage ?</li>
</ul>

<p>Questions suppl&eacute;mentaires que vous pouvez poser:</p>

<ul>
	<li>Qu&rsquo;est-ce que ses disciples apprennent?</li>
	<li>Qu&rsquo;est-ce que J&eacute;sus est en train de nous montrer au sujet de sa vie et de son minist&egrave;re (ou leadership) ?</li>
	<li>Qu&rsquo;est ce que J&eacute;sus est en train de montrer au sujet du leadership empreint de pi&eacute;t&eacute; ?</li>
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

<p>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</p>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<p>Jean a d&eacute;m&eacute;nag&eacute; son minist&egrave;re au nord de la Jud&eacute;e et a commenc&eacute; &agrave; baptiser les gens sur le bord de la r&eacute;gion de la D&eacute;capole et en Samarie. J&eacute;sus a continu&eacute; son minist&egrave;re dans la campagne de la Jud&eacute;e tandis que Jean a continu&eacute; son minist&egrave;re de pr&eacute;parer le chemin pour que les gens viennent &agrave; J&eacute;sus. Comme les disciples de Jean demandent pourquoi le minist&egrave;re de J&eacute;sus devenait plus grand que celui de Jean, Jean explique sa perspective: il savait qui &eacute;tait J&eacute;sus et qui il &eacute;tait, il savait que la source de la vraie joie &eacute;tait d&#39;&ecirc;tre pr&egrave;s de J&eacute;sus et d&#39;&eacute;couter sa voix, et il savait qu&rsquo;apr&egrave;s avoir entendu J&eacute;sus parler, il ne pouvait qu&#39;ob&eacute;ir. Jean a montr&eacute; comment mourir &agrave; soi et &ecirc;tre ob&eacute;issant &agrave; la volont&eacute; du P&egrave;re.</p>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ Se Pr&eacute;parer pour la Mission</h2></div>
<div class="collapsed" id ="Text3">
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

<h2>Aller en Mission</h2>

<ul>
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

<p>&nbsp;</p>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'La source de la Vraie Joie: ', '/content/M2/fra/multiply2/multiply212.html')">
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