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
                        <div class="chapter_number ltr"><h1>19.</h1></div>
                        <div class="chapter_title ltr"><h1>Deuxième Expédition de la Pêche d’hommes</h1></div>
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
	<li>Lisez ou observez Marc 1 :29-39 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Marc 1:29-39</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">29&nbsp;</sup>En sortant de la synagogue, ils se rendirent avec Jacques et Jean &agrave; la maison de Simon et d&#39;Andr&eacute;.</p>

<p><sup class="versenum">30&nbsp;</sup>La belle-m&egrave;re de Simon &eacute;tait couch&eacute;e, ayant la fi&egrave;vre; et aussit&ocirc;t on parla d&#39;elle &agrave; J&eacute;sus.</p>

<p><sup class="versenum">31&nbsp;</sup>S&#39;&eacute;tant approch&eacute;, il la fit lever en lui prenant la main, et &agrave; l&#39;instant la fi&egrave;vre la quitta. Puis elle les servit.</p>

<p><sup class="versenum">32&nbsp;</sup>Le soir, apr&egrave;s le coucher du soleil, on lui amena tous les malades et les d&eacute;moniaques.</p>

<p><sup class="versenum">33&nbsp;</sup>Et toute la ville &eacute;tait rassembl&eacute;e devant sa porte.</p>

<p><sup class="versenum">34&nbsp;</sup>Il gu&eacute;rit beaucoup de gens qui avaient diverses maladies; il chassa aussi beaucoup de d&eacute;mons, et il ne permettait pas aux d&eacute;mons de parler, parce qu&#39;ils le connaissaient.</p>

<p><sup class="versenum">35&nbsp;</sup>Vers le matin, pendant qu&#39;il faisait encore tr&egrave;s sombre, il se leva, et sortit pour aller dans un lieu d&eacute;sert, o&ugrave; il pria.</p>

<p><sup class="versenum">36&nbsp;</sup>Simon et ceux qui &eacute;taient avec lui se mirent &agrave; sa recherche;</p>

<p><sup class="versenum">37&nbsp;</sup>et, quand ils l&#39;eurent trouv&eacute;, ils lui dirent: Tous te cherchent.</p>

<p><sup class="versenum">38&nbsp;</sup>Il leur r&eacute;pondit: Allons ailleurs, dans les bourgades voisines, afin que j&#39;y pr&ecirc;che aussi; car c&#39;est pour cela que je suis sorti.</p>

<p><sup class="versenum">39&nbsp;</sup>Et il alla pr&ecirc;cher dans les synagogues, par toute la Galil&eacute;e, et il chassa les d&eacute;mons.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/219.mp4" type="button" class="external-movie">
         Regardez &nbsp;Marc 1:29-39&nbsp; </button>
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

<p>La deuxi&egrave;me campagne de J&eacute;sus est &agrave; la maison de Pierre. C&#39;est une &eacute;vang&eacute;lisation &agrave; domicile qui a commenc&eacute; le soir apr&egrave;s le coucher du soleil. Des gens de toute la r&eacute;gion sont venus voir l&#39;homme qui avait chass&eacute; un d&eacute;mon dans la synagogue. C&#39;&eacute;tait une campagne spontan&eacute;e qui a dur&eacute; plusieurs heures dans la nuit. Apr&egrave;s une longue nuit de minist&egrave;re, J&eacute;sus se l&egrave;ve t&ocirc;t et sort de la maison pour se retrouver seul avec le P&egrave;re. Il a montr&eacute; la priorit&eacute; de se retrouver seul avec le P&egrave;re, d&#39;entendre Sa voix, de d&eacute;couvrir les prochaines &eacute;tapes de la vie et du minist&egrave;re et de juste communier avec Lui. M&ecirc;me si tout le monde voulait qu&#39;il reste et ait un minist&egrave;re plus r&eacute;ussi, il a quitt&eacute; en ob&eacute;issance au P&egrave;re et la port&eacute;e de sa mission.</p>

<ul>
	<li class="nobreak-final-final">Etude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Luc 4:38-44</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">38&nbsp;</sup>En sortant de la synagogue, il se rendit &agrave; la maison de Simon. La belle-m&egrave;re de Simon avait une violente fi&egrave;vre, et ils le pri&egrave;rent en sa faveur.</p>

	<p><sup class="versenum">39&nbsp;</sup>S&#39;&eacute;tant pench&eacute; sur elle, il mena&ccedil;a la fi&egrave;vre, et la fi&egrave;vre la quitta. A l&#39;instant elle se leva, et les servit.</p>

	<p><sup class="versenum">40&nbsp;</sup>Apr&egrave;s le couch&eacute; du soleil, tous ceux qui avaient des malades atteints de diverses maladies les lui amen&egrave;rent. Il imposa les mains &agrave; chacun d&#39;eux, et il les gu&eacute;rit.</p>

	<p><sup class="versenum">41&nbsp;</sup>Des d&eacute;mons aussi sortirent de beaucoup de personnes, en criant et en disant: Tu es le Fils de Dieu. Mais il les mena&ccedil;ait et ne leur permettait pas de parler, parce qu&#39;ils savaient qu&#39;il &eacute;tait le Christ.</p>

	<p><sup class="versenum">42&nbsp;</sup>D&egrave;s que le jour parut, il sortit et alla dans un lieu d&eacute;sert. Une foule de gens se mirent &agrave; sa recherche, et arriv&egrave;rent jusqu&#39;&agrave; lui; ils voulaient le retenir, afin qu&#39;il ne les quitt&acirc;t point.</p>

	<p><sup class="versenum">43&nbsp;</sup>Mais il leur dit: Il faut aussi que j&#39;annonce aux autres villes la bonne nouvelle du royaume de Dieu; car c&#39;est pour cela que j&#39;ai &eacute;t&eacute; envoy&eacute;.</p>

	<p><sup class="versenum">44&nbsp;</sup>Et il pr&ecirc;chait dans les synagogues de la Galil&eacute;e.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> Matthieu 8:14-17</span>

	<div class="popup invisible" id="pop2">
	<p><sup class="versenum">15&nbsp;</sup>Il toucha sa main, et la fi&egrave;vre la quitta; puis elle se leva, et le servit.</p>

	<p><sup class="versenum">16&nbsp;</sup>Le soir, on amena aupr&egrave;s de J&eacute;sus plusieurs d&eacute;moniaques. Il chassa les esprits par sa parole, et il gu&eacute;rit tous les malades,</p>

	<p><sup class="versenum">17&nbsp;</sup>afin que s&#39;accompl&icirc;t ce qui avait &eacute;t&eacute; annonc&eacute; par &Eacute;sa&iuml;e, le proph&egrave;te: Il a pris nos infirmit&eacute;s, et il s&#39;est charg&eacute; de nos maladies.</p>
	<sup class="versenum">14&nbsp;</sup>J&eacute;sus se rendit ensuite &agrave; la maison de Pierre, dont il vit la belle-m&egrave;re couch&eacute;e et ayant la fi&egrave;vre.<!-- end bible --></div>
	</li>
</ul>

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

			<td class="social" @click="share('lesson', 'Deuxième Expédition de la Pêche d’hommes: ', '/content/M2/fra/multiply2/multiply219.html')">
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