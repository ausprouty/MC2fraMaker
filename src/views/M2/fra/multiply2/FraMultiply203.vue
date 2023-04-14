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
                        <div class="chapter_number ltr"><h1>3.</h1></div>
                        <div class="chapter_title ltr"><h1>Jésus comme un Enfant</h1></div>
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
	<li>Lisez ou observez Matthieu 2:1-18 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Matthieu 2:1-18</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>J&eacute;sus &eacute;tant n&eacute; &agrave; Bethl&eacute;hem en Jud&eacute;e, au temps du roi H&eacute;rode, voici des mages d&#39;Orient arriv&egrave;rent &agrave; J&eacute;rusalem,</p>

<p><sup class="versenum">2&nbsp;</sup>et dirent: O&ugrave; est le roi des Juifs qui vient de na&icirc;tre? car nous avons vu son &eacute;toile en Orient, et nous sommes venus pour l&#39;adorer.</p>

<p><sup class="versenum">3&nbsp;</sup>Le roi H&eacute;rode, ayant appris cela, fut troubl&eacute;, et tout J&eacute;rusalem avec lui.</p>

<p><sup class="versenum">4&nbsp;</sup>Il assembla tous les principaux sacrificateurs et les scribes du peuple, et il s&#39;informa aupr&egrave;s d&#39;eux o&ugrave; devait na&icirc;tre le Christ.</p>

<p><sup class="versenum">5&nbsp;</sup>Ils lui dirent: A Bethl&eacute;hem en Jud&eacute;e; car voici ce qui a &eacute;t&eacute; &eacute;crit par le proph&egrave;te:</p>

<p><sup class="versenum">6&nbsp;</sup>Et toi, Bethl&eacute;hem, terre de Juda, Tu n&#39;es certes pas la moindre entre les principales villes de Juda, Car de toi sortira un chef Qui pa&icirc;tra Isra&euml;l, mon peuple.</p>

<p><sup class="versenum">7&nbsp;</sup>Alors H&eacute;rode fit appeler en secret les mages, et s&#39;enquit soigneusement aupr&egrave;s d&#39;eux depuis combien de temps l&#39;&eacute;toile brillait.</p>

<p><sup class="versenum">8&nbsp;</sup>Puis il les envoya &agrave; Bethl&eacute;hem, en disant: Allez, et prenez des informations exactes sur le petit enfant; quand vous l&#39;aurez trouv&eacute;, faites-le-moi savoir, afin que j&#39;aille aussi moi-m&ecirc;me l&#39;adorer.</p>

<p><sup class="versenum">9&nbsp;</sup>Apr&egrave;s avoir entendu le roi, ils partirent. Et voici, l&#39;&eacute;toile qu&#39;ils avaient vue en Orient marchait devant eux jusqu&#39;&agrave; ce qu&#39;&eacute;tant arriv&eacute;e au-dessus du lieu o&ugrave; &eacute;tait le petit enfant, elle s&#39;arr&ecirc;ta.</p>

<p><sup class="versenum">10&nbsp;</sup>Quand ils aper&ccedil;urent l&#39;&eacute;toile, ils furent saisis d&#39;une tr&egrave;s grande joie.</p>

<p><sup class="versenum">11&nbsp;</sup>Ils entr&egrave;rent dans la maison, virent le petit enfant avec Marie, sa m&egrave;re, se prostern&egrave;rent et l&#39;ador&egrave;rent; ils ouvrirent ensuite leurs tr&eacute;sors, et lui offrirent en pr&eacute;sent de l&#39;or, de l&#39;encens et de la myrrhe.</p>

<p><sup class="versenum">12&nbsp;</sup>Puis, divinement avertis en songe de ne pas retourner vers H&eacute;rode, ils regagn&egrave;rent leur pays par un autre chemin.</p>

<p><sup class="versenum">13&nbsp;</sup>Lorsqu&#39;ils furent partis, voici, un ange du Seigneur apparut en songe &agrave; Joseph, et dit: L&egrave;ve-toi, prends le petit enfant et sa m&egrave;re, fuis en &Eacute;gypte, et restes-y jusqu&#39;&agrave; ce que je te parle; car H&eacute;rode cherchera le petit enfant pour le faire p&eacute;rir.</p>

<p><sup class="versenum">14&nbsp;</sup>Joseph se leva, prit de nuit le petit enfant et sa m&egrave;re, et se retira en &Eacute;gypte.</p>

<p><sup class="versenum">15&nbsp;</sup>Il y resta jusqu&#39;&agrave; la mort d&#39;H&eacute;rode, afin que s&#39;accompl&icirc;t ce que le Seigneur avait annonc&eacute; par le proph&egrave;te: J&#39;ai appel&eacute; mon fils hors d&#39;&Eacute;gypte.</p>

<p><sup class="versenum">16&nbsp;</sup>Alors H&eacute;rode, voyant qu&#39;il avait &eacute;t&eacute; jou&eacute; par les mages, se mit dans une grande col&egrave;re, et il envoya tuer tous les enfants de deux ans et au-dessous qui &eacute;taient &agrave; Bethl&eacute;hem et dans tout son territoire, selon la date dont il s&#39;&eacute;tait soigneusement enquis aupr&egrave;s des mages.</p>

<p><sup class="versenum">17&nbsp;</sup>Alors s&#39;accomplit ce qui avait &eacute;t&eacute; annonc&eacute; par J&eacute;r&eacute;mie, le proph&egrave;te:</p>

<p><sup class="versenum">18&nbsp;</sup>On a entendu des cris &agrave; Rama, Des pleurs et de grandes lamentations: Rachel pleure ses enfants, Et n&#39;a pas voulu &ecirc;tre consol&eacute;e, Parce qu&#39;ils ne sont plus.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/203.mp4" type="button" class="external-movie">
         Regardez &nbsp;Matthieu 2:1-18&nbsp; </button>
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

<p>Apr&egrave;s que J&eacute;sus naquit, Dieu envoya des provisions &agrave; la famille par les astrologues Gentils (non-juifs). Leurs cadeaux furent probablement utilis&eacute;s pour aider la famille &agrave; faire le voyage pour l&rsquo;Egypte. Le P&egrave;re pourvoit toujours aux besoins de son Fils J&eacute;sus. Et Dieu pourvoit toujours aux besoins de ses enfants. Quelquefois, la provision vient la nuit qui pr&eacute;c&egrave;de le jour o&ugrave; vous en avez besoin, quelquefois, elle vient des jours avant et quelquefois pendant que vous marchez par la foi vers l&rsquo;endroit o&ugrave; Dieu vous conduit.</p>

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

			<td class="social" @click="share('lesson', 'Jésus comme un Enfant: ', '/content/M2/fra/multiply2/multiply203.html')">
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