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
                        <div class="chapter_number ltr"><h1>8.</h1></div>
                        <div class="chapter_title ltr"><h1>Viens et vois, suis Moi</h1></div>
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
	<li>Lisez ou observez 1:19-51 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 1:19-51</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">19&nbsp;</sup>Voici le t&eacute;moignage de Jean, lorsque les Juifs envoy&egrave;rent de J&eacute;rusalem des sacrificateurs et des L&eacute;vites, pour lui demander: Toi, qui es-tu?</p>

<p><sup class="versenum">20&nbsp;</sup>Il d&eacute;clara, et ne le nia point, il d&eacute;clara qu&#39;il n&#39;&eacute;tait pas le Christ.</p>

<p><sup class="versenum">21&nbsp;</sup>Et ils lui demand&egrave;rent: Quoi donc? es-tu &Eacute;lie? Et il dit: Je ne le suis point. Es-tu le proph&egrave;te? Et il r&eacute;pondit: Non.</p>

<p><sup class="versenum">22&nbsp;</sup>Ils lui dirent alors: Qui es-tu? afin que nous donnions une r&eacute;ponse &agrave; ceux qui nous ont envoy&eacute;s. Que dis-tu de toi-m&ecirc;me?</p>

<p><sup class="versenum">23&nbsp;</sup>Moi, dit-il, je suis la voix de celui qui crie dans le d&eacute;sert: Aplanissez le chemin du Seigneur, comme a dit &Eacute;sa&iuml;e, le proph&egrave;te.</p>

<p><sup class="versenum">24&nbsp;</sup>Ceux qui avaient &eacute;t&eacute; envoy&eacute;s &eacute;taient des pharisiens.</p>

<p><sup class="versenum">25&nbsp;</sup>Ils lui firent encore cette question: Pourquoi donc baptises-tu, si tu n&#39;es pas le Christ, ni &Eacute;lie, ni le proph&egrave;te?</p>

<p><sup class="versenum">26&nbsp;</sup>Jean leur r&eacute;pondit: Moi, je baptise d&#39;eau, mais au milieu de vous il y a quelqu&#39;un que vous ne connaissez pas, qui vient apr&egrave;s moi;</p>

<p><sup class="versenum">27&nbsp;</sup>je ne suis pas digne de d&eacute;lier la courroie de ses souliers.</p>

<p><sup class="versenum">28&nbsp;</sup>Ces choses se pass&egrave;rent &agrave; B&eacute;thanie, au del&agrave; du Jourdain, o&ugrave; Jean baptisait.</p>

<p><sup class="versenum">29&nbsp;</sup>Le lendemain, il vit J&eacute;sus venant &agrave; lui, et il dit: Voici l&#39;Agneau de Dieu, qui &ocirc;te le p&eacute;ch&eacute; du monde.</p>

<p><sup class="versenum">30&nbsp;</sup>C&#39;est celui dont j&#39;ai dit: Apr&egrave;s moi vient un homme qui m&#39;a pr&eacute;c&eacute;d&eacute;, car il &eacute;tait avant moi.</p>

<p><sup class="versenum">31&nbsp;</sup>Je ne le connaissais pas, mais c&#39;est afin qu&#39;il f&ucirc;t manifest&eacute; &agrave; Isra&euml;l que je suis venu baptiser d&#39;eau.</p>

<p><sup class="versenum">32&nbsp;</sup>Jean rendit ce t&eacute;moignage: J&#39;ai vu l&#39;Esprit descendre du ciel comme une colombe et s&#39;arr&ecirc;ter sur lui.</p>

<p><sup class="versenum">33&nbsp;</sup>Je ne le connaissais pas, mais celui qui m&#39;a envoy&eacute; baptiser d&#39;eau, celui-l&agrave; m&#39;a dit: Celui sur qui tu verras l&#39;Esprit descendre et s&#39;arr&ecirc;ter, c&#39;est celui qui baptise du Saint Esprit.</p>

<p><sup class="versenum">34&nbsp;</sup>Et j&#39;ai vu, et j&#39;ai rendu t&eacute;moignage qu&#39;il est le Fils de Dieu.</p>

<p><sup class="versenum">35&nbsp;</sup>Le lendemain, Jean &eacute;tait encore l&agrave;, avec deux de ses disciples;</p>

<p><sup class="versenum">36&nbsp;</sup>et, ayant regard&eacute; J&eacute;sus qui passait, il dit: Voil&agrave; l&#39;Agneau de Dieu.</p>

<p><sup class="versenum">37&nbsp;</sup>Les deux disciples l&#39;entendirent prononcer ces paroles, et ils suivirent J&eacute;sus.</p>

<p><sup class="versenum">38&nbsp;</sup>J&eacute;sus se retourna, et voyant qu&#39;ils le suivaient, il leur dit: Que cherchez-vous? Ils lui r&eacute;pondirent: Rabbi (ce qui signifie Ma&icirc;tre), o&ugrave; demeures-tu?</p>

<p><sup class="versenum">39&nbsp;</sup>Venez, leur dit-il, et voyez. Ils all&egrave;rent, et ils virent o&ugrave; il demeurait; et ils rest&egrave;rent aupr&egrave;s de lui ce jour-l&agrave;. C&#39;&eacute;tait environ la dixi&egrave;me heure.</p>

<p><sup class="versenum">40&nbsp;</sup>Andr&eacute;, fr&egrave;re de Simon Pierre, &eacute;tait l&#39;un des deux qui avaient entendu les paroles de Jean, et qui avaient suivi J&eacute;sus.</p>

<p><sup class="versenum">41&nbsp;</sup>Ce fut lui qui rencontra le premier son fr&egrave;re Simon, et il lui dit: Nous avons trouv&eacute; le Messie (ce qui signifie Christ).</p>

<p><sup class="versenum">42&nbsp;</sup>Et il le conduisit vers J&eacute;sus. J&eacute;sus, l&#39;ayant regard&eacute;, dit: Tu es Simon, fils de Jonas; tu seras appel&eacute; C&eacute;phas (ce qui signifie Pierre).</p>

<p><sup class="versenum">43&nbsp;</sup>Le lendemain, J&eacute;sus voulut se rendre en Galil&eacute;e, et il rencontra Philippe. Il lui dit: Suis-moi.</p>

<p><sup class="versenum">44&nbsp;</sup>Philippe &eacute;tait de Bethsa&iuml;da, de la ville d&#39;Andr&eacute; et de Pierre.</p>

<p><sup class="versenum">45&nbsp;</sup>Philippe rencontra Nathana&euml;l, et lui dit: Nous avons trouv&eacute; celui de qui Mo&iuml;se a &eacute;crit dans la loi et dont les proph&egrave;tes ont parl&eacute;, J&eacute;sus de Nazareth, fils de Joseph.</p>

<p><sup class="versenum">46&nbsp;</sup>Nathana&euml;l lui dit: Peut-il venir de Nazareth quelque chose de bon? Philippe lui r&eacute;pondit: Viens, et vois.</p>

<p><sup class="versenum">47&nbsp;</sup>J&eacute;sus, voyant venir &agrave; lui Nathana&euml;l, dit de lui: Voici vraiment un Isra&eacute;lite, dans lequel il n&#39;y a point de fraude.</p>

<p><sup class="versenum">48&nbsp;</sup>D&#39;o&ugrave; me connais-tu? lui dit Nathana&euml;l. J&eacute;sus lui r&eacute;pondit: Avant que Philippe t&#39;appel&acirc;t, quand tu &eacute;tais sous le figuier, je t&#39;ai vu.</p>

<p><sup class="versenum">49&nbsp;</sup>Nathana&euml;l r&eacute;pondit et lui dit: Rabbi, tu es le Fils de Dieu, tu es le roi d&#39;Isra&euml;l.</p>

<p><sup class="versenum">50&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Parce que je t&#39;ai dit que je t&#39;ai vu sous le figuier, tu crois; tu verras de plus grandes choses que celles-ci.</p>

<p><sup class="versenum">51&nbsp;</sup>Et il lui dit: En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, vous verrez d&eacute;sormais le ciel ouvert et les anges de Dieu monter et descendre sur le Fils de l&#39;homme.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/208.mp4" type="button" class="external-movie">
         Regardez Jean 1:19-51 </button>
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

<p>Apr&egrave;s 40 jours dans le d&eacute;sert, J&eacute;sus commence sa mission qu&rsquo;est de faire des disciples. Il commence par nous montrer un style de vie qui consiste &agrave; rechercher les relations accept&eacute;es. Andr&eacute;, Pierre, Jean, Philippe, et Nathana&euml;l se connaissaient tous. Il commence &agrave; appeler les gens &agrave; &laquo; venir et voir &raquo; (venir investiguer les faits) qui Il est. Il ouvrit alors leurs yeux sur la v&eacute;rit&eacute; selon laquelle Il est le Messie promis. Puisqu&rsquo;ils croient, Il change Son message en &laquo; suivez-moi &raquo; deux appels, un &agrave; l&rsquo;endroit de ceux qui n&rsquo;ont pas encore cru et un &agrave; l&rsquo;endroit de ceux qui croient.</p>

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

			<td class="social" @click="share('lesson', 'Viens et vois, suis Moi: ', '/content/M2/fra/multiply2/multiply208.html')">
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