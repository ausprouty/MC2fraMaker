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
                        <div class="chapter_number ltr"><h1>37.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership et la Peur</h1></div>
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
	<li>Lisez ou observez Matthieu 14:22-33 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Matthieu 14:22-33</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">22&nbsp;</sup>Aussit&ocirc;t apr&egrave;s, il obligea les disciples &agrave; monter dans la barque et &agrave; passer avant lui de l&#39;autre c&ocirc;t&eacute;, pendant qu&#39;il renverrait la foule.</p>

<p><sup class="versenum">23&nbsp;</sup>Quand il l&#39;eut renvoy&eacute;e, il monta sur la montagne, pour prier &agrave; l&#39;&eacute;cart; et, comme le soir &eacute;tait venu, il &eacute;tait l&agrave; seul.</p>

<p><sup class="versenum">24&nbsp;</sup>La barque, d&eacute;j&agrave; au milieu de la mer, &eacute;tait battue par les flots; car le vent &eacute;tait contraire.</p>

<p><sup class="versenum">25&nbsp;</sup>A la quatri&egrave;me veille de la nuit, J&eacute;sus alla vers eux, marchant sur la mer.</p>

<p><sup class="versenum">26&nbsp;</sup>Quand les disciples le virent marcher sur la mer, ils furent troubl&eacute;s, et dirent: C&#39;est un fant&ocirc;me! Et, dans leur frayeur, ils pouss&egrave;rent des cris.</p>

<p><sup class="versenum">27&nbsp;</sup>J&eacute;sus leur dit aussit&ocirc;t: Rassurez-vous, c&#39;est moi; n&#39;ayez pas peur!</p>

<p><sup class="versenum">28&nbsp;</sup>Pierre lui r&eacute;pondit: Seigneur, si c&#39;est toi, ordonne que j&#39;aille vers toi sur les eaux.</p>

<p><sup class="versenum">29&nbsp;</sup>Et il dit: Viens! Pierre sortit de la barque, et marcha sur les eaux, pour aller vers J&eacute;sus.</p>

<p><sup class="versenum">30&nbsp;</sup>Mais, voyant que le vent &eacute;tait fort, il eut peur; et, comme il commen&ccedil;ait &agrave; enfoncer, il s&#39;&eacute;cria: Seigneur, sauve-moi!</p>

<p><sup class="versenum">31&nbsp;</sup>Aussit&ocirc;t J&eacute;sus &eacute;tendit la main, le saisit, et lui dit: Homme de peu de foi, pourquoi as-tu dout&eacute;?</p>

<p><sup class="versenum">32&nbsp;</sup>Et ils mont&egrave;rent dans la barque, et le vent cessa.</p>

<p><sup class="versenum">33&nbsp;</sup>Ceux qui &eacute;taient dans la barque vinrent se prosterner devant J&eacute;sus, et dirent: Tu es v&eacute;ritablement le Fils de Dieu.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/237.mp4" type="button" class="external-movie">
         Regardez &nbsp;Matthieu 14:22-33&nbsp; </button>
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

<p>J&eacute;sus a fait sortir ses disciples sur l&#39;eau pendant qu&#39;il cherchait le temps pour rester seul avec le P&egrave;re. Bizarrement, Il les a intentionnellement envoy&eacute; dans une temp&ecirc;te et a regard&eacute; ses leaders lutter pendant un moment. Alors J&eacute;sus est all&eacute; &agrave; eux en marchant sur l&#39;eau. &Eacute;tant fatigu&eacute;s et effray&eacute;s, ils ont commenc&eacute; &agrave; crier &laquo;C&#39;est un fant&ocirc;me!&raquo; Alors que J&eacute;sus essaie de les r&eacute;conforter, Pierre montre sa foi audacieuse en voulant aller vers J&eacute;sus sur l&#39;eau. Pierre a bien tenu jusqu&#39;&agrave; ce qu&#39;il d&eacute;tourne ses regards de J&eacute;sus. Alors que Pierre crie pour &ecirc;tre sauv&eacute;, J&eacute;sus le secourt imm&eacute;diatement. Les 12 savaient qu&#39;ils &eacute;taient en pr&eacute;sence du Fils de Dieu et l&#39;adoraient en r&eacute;ponse.</p>

<ul>
	<li class="nobreak-final-final">Pour une &eacute;tude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Marc 6:45-52</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">45&nbsp;</sup>Aussit&ocirc;t apr&egrave;s, il obligea ses disciples &agrave; monter dans la barque et &agrave; passer avant lui de l&#39;autre c&ocirc;t&eacute;, vers Bethsa&iuml;da, pendant que lui-m&ecirc;me renverrait la foule.</p>

	<p><sup class="versenum">46&nbsp;</sup>Quand il l&#39;eut renvoy&eacute;e, il s&#39;en alla sur la montagne, pour prier.</p>

	<p><sup class="versenum">47&nbsp;</sup>Le soir &eacute;tant venu, la barque &eacute;tait au milieu de la mer, et J&eacute;sus &eacute;tait seul &agrave; terre.</p>

	<p><sup class="versenum">48&nbsp;</sup>Il vit qu&#39;ils avaient beaucoup de peine &agrave; ramer; car le vent leur &eacute;tait contraire. A la quatri&egrave;me veille de la nuit environ, il alla vers eux, marchant sur la mer, et il voulait les d&eacute;passer.</p>

	<p><sup class="versenum">49&nbsp;</sup>Quand ils le virent marcher sur la mer, ils crurent que c&#39;&eacute;taient un fant&ocirc;me, et ils pouss&egrave;rent des cris;</p>

	<p><sup class="versenum">50&nbsp;</sup>car ils le voyaient tous, et ils &eacute;taient troubl&eacute;s. Aussit&ocirc;t J&eacute;sus leur parla, et leur dit: Rassurez-vous, c&#39;est moi, n&#39;ayez pas peur!</p>

	<p><sup class="versenum">51&nbsp;</sup>Puis il monta vers eux dans la barque, et le vent cessa. Ils furent en eux-m&ecirc;me tout stup&eacute;faits et remplis d&#39;&eacute;tonnement;</p>

	<p><sup class="versenum">52&nbsp;</sup>car ils n&#39;avaient pas compris le miracle des pains, parce que leur coeur &eacute;tait endurci.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> Jean 6:16-21</span>.

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">16&nbsp;</sup>Quand le soir fut venu, ses disciples descendirent au bord de la mer.</p>

	<p><sup class="versenum">17&nbsp;</sup>&Eacute;tant mont&eacute;s dans une barque, ils traversaient la mer pour se rendre &agrave; Caperna&uuml;m. Il faisait d&eacute;j&agrave; nuit, et J&eacute;sus ne les avait pas encore rejoints.</p>

	<p><sup class="versenum">18&nbsp;</sup>Il soufflait un grand vent, et la mer &eacute;tait agit&eacute;e.</p>

	<p><sup class="versenum">19&nbsp;</sup>Apr&egrave;s avoir ram&eacute; environ vingt-cinq ou trente stades, ils virent J&eacute;sus marchant sur la mer et s&#39;approchant de la barque. Et ils eurent peur.</p>

	<p><sup class="versenum">20&nbsp;</sup>Mais J&eacute;sus leur dit: C&#39;est moi; n&#39;ayez pas peur!</p>

	<p><sup class="versenum">21&nbsp;</sup>Ils voulaient donc le prendre dans la barque, et aussit&ocirc;t la barque aborda au lieu o&ugrave; ils allaient.</p>
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

			<td class="social" @click="share('lesson', 'Leadership et la Peur: ', '/content/M2/fra/multiply2/multiply237.html')">
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