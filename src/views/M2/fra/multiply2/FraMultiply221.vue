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
                        <div class="chapter_number ltr"><h1>21.</h1></div>
                        <div class="chapter_title ltr"><h1>Quatrième Expédition de la Pêche d’hommes:</h1></div>
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
	<li>Lisez ou observez Luc 5:12-16 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 5:12-16</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">12&nbsp;</sup>J&eacute;sus &eacute;tait dans une des villes; et voici, un homme couvert de l&egrave;pre, l&#39;ayant vu, tomba sur sa face, et lui fit cette pri&egrave;re: Seigneur, si tu le veux, tu peux me rendre pur.</p>

<p><sup class="versenum">13&nbsp;</sup>J&eacute;sus &eacute;tendit la main, le toucha, et dit: Je le veux, sois pur. Aussit&ocirc;t la l&egrave;pre le quitta.</p>

<p><sup class="versenum">14&nbsp;</sup>Puis il lui ordonna de n&#39;en parler &agrave; personne. Mais, dit-il, va te montrer au sacrificateur, et offre pour ta purification ce que Mo&iuml;se a prescrit, afin que cela leur serve de t&eacute;moignage.</p>

<p><sup class="versenum">15&nbsp;</sup>Sa renomm&eacute;e se r&eacute;pandait de plus en plus, et les gens venaient en foule pour l&#39;entendre et pour &ecirc;tre gu&eacute;ris de leurs maladies.</p>

<p><sup class="versenum">16&nbsp;</sup>Et lui, il se retirait dans les d&eacute;serts, et priait.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/221.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 5:12-16&nbsp; </button>
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

<p>J&eacute;sus et les disciples voyagent contr&eacute;e en contr&eacute;e et de ville en ville. Dans une ville, il rencontre un homme couvert de l&egrave;pre. La l&egrave;pre &eacute;tait une maladie tr&egrave;s contagieuse et si vous l&#39;aviez, vous deveniez un paria social et religieux et n&#39;aviez aucun espoir. Vous &ecirc;tes rejet&eacute; de la soci&eacute;t&eacute; et pris pour un condamn&eacute; par Dieu ; alors seul Dieu pouvait la gu&eacute;rir. J&eacute;sus &eacute;tait &eacute;mu de compassion et n&#39;avait pas peur de la l&egrave;pre de l&#39;homme. J&eacute;sus a montr&eacute; comment aimer le paria, le d&eacute;testable, le rejet&eacute; social et les a p&ecirc;ch&eacute;s. J&eacute;sus a ordonn&eacute; &agrave; l&#39;homme d&#39;aller se montrer au pr&ecirc;tre comme un t&eacute;moignage pour eux que le Messie &eacute;tait venu. Cet homme est sorti et a commenc&eacute; &agrave; parler librement de J&eacute;sus et par cons&eacute;quent, J&eacute;sus ne pouvait plus entrer ouvertement dans une ville. (<span class="popup-link" @click = "popUp('pop1')"> Marc 1:45</span>).</p>

<div class="popup invisible" id="pop1"><!-- begin bible -->
<p><sup class="versenum">45&nbsp;</sup>Mais cet homme, s&#39;en &eacute;tant all&eacute;, se mit &agrave; publier hautement la chose et &agrave; la divulguer, de sorte que J&eacute;sus ne pouvait plus entrer publiquement dans une ville. Il se tenait dehors, dans des lieux d&eacute;serts, et l&#39;on venait &agrave; lui de toutes parts.</p>
</div>

<ul>
	<li class="nobreak-final-final">Etude approfondie: <span class="popup-link" @click = "popUp('pop2')">  Matthieu 8:2-4</span>;&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">2&nbsp;</sup>Et voici, un l&eacute;preux s&#39;&eacute;tant approch&eacute; se prosterna devant lui, et dit: Seigneur, si tu le veux, tu peux me rendre pur.</p>

	<p><sup class="versenum">3&nbsp;</sup>J&eacute;sus &eacute;tendit la main, le toucha, et dit: Je le veux, sois pur. Aussit&ocirc;t il fut purifi&eacute; de sa l&egrave;pre.</p>

	<p><sup class="versenum">4&nbsp;</sup>Puis J&eacute;sus lui dit: Garde-toi d&#39;en parler &agrave; personne; mais va te montrer au sacrificateur, et pr&eacute;sente l&#39;offrande que Mo&iuml;se a prescrite, afin que cela leur serve de t&eacute;moignage.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop3')"> Marc 1:40-45</span>.&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">40&nbsp;</sup>Un l&eacute;preux vint &agrave; lui; et, se jetant &agrave; genoux, il lui dit d&#39;un ton suppliant: Si tu le veux, tu peux me rendre pur.</p>

	<p><sup class="versenum">41&nbsp;</sup>J&eacute;sus, &eacute;mu de compassion, &eacute;tendit la main, le toucha, et dit: Je le veux, sois pur.</p>

	<p><sup class="versenum">42&nbsp;</sup>Aussit&ocirc;t la l&egrave;pre le quitta, et il fut purifi&eacute;.</p>

	<p><sup class="versenum">43&nbsp;</sup>J&eacute;sus le renvoya sur-le-champ, avec de s&eacute;v&egrave;res recommandations,</p>

	<p><sup class="versenum">44&nbsp;</sup>et lui dit: Garde-toi de rien dire &agrave; personne; mais va te montrer au sacrificateur, et offre pour ta purification ce que Mo&iuml;se a prescrit, afin que cela leur serve de t&eacute;moignage.</p>

	<p><sup class="versenum">45&nbsp;</sup>Mais cet homme, s&#39;en &eacute;tant all&eacute;, se mit &agrave; publier hautement la chose et &agrave; la divulguer, de sorte que J&eacute;sus ne pouvait plus entrer publiquement dans une ville. Il se tenait dehors, dans des lieux d&eacute;serts, et l&#39;on venait &agrave; lui de toutes parts.</p>
	<!-- end bible --></div>
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

			<td class="social" @click="share('lesson', 'Quatrième Expédition de la Pêche d’hommes:: ', '/content/M2/fra/multiply2/multiply221.html')">
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