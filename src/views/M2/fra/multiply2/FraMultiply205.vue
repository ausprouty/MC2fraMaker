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
                        <div class="chapter_number ltr"><h1>5.</h1></div>
                        <div class="chapter_title ltr"><h1>Jésus comme un Jeune Homme et Charpentier/Constructeur</h1></div>
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
	<li>Lisez ou observez Matthieu 13:55-56; Psaumes 69:7-12; Marc 6:3 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Matthieu 13:55-56</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">55&nbsp;</sup>N&#39;est-ce pas le fils du charpentier? n&#39;est-ce pas Marie qui est sa m&egrave;re? Jacques, Joseph, Simon et Jude, ne sont-ils pas ses fr&egrave;res?</p>

<p><sup class="versenum">56&nbsp;</sup>et ses soeurs ne sont-elles pas toutes parmi nous? D&#39;o&ugrave; lui viennent donc toutes ces choses?</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/205.mp4" type="button" class="external-movie">
         Regardez &nbsp;Matthieu 13:55-56&nbsp; </button>
    <div class="collapsed"></div>

<button id="Button1" type="button" class="collapsible bible">Lire Psaumes 69:7-12</button><div class="collapsed" id ="Text1">
<!-- begin bible -->

<p><sup class="versenum">7&nbsp;</sup>(69:8) Car c&#39;est pour toi que je porte l&#39;opprobre, Que la honte couvre mon visage;</p>

<p><sup class="versenum">8&nbsp;</sup>(69:9) Je suis devenu un &eacute;tranger pour mes fr&egrave;res, Un inconnu pour les fils de ma m&egrave;re.</p>

<p><sup class="versenum">9&nbsp;</sup>(69:10) Car le z&egrave;le de ta maison me d&eacute;vore, Et les outrages de ceux qui t&#39;insultent tombent sur moi.</p>

<p><sup class="versenum">10&nbsp;</sup>(69:11) Je verse des larmes et je je&ucirc;ne, Et c&#39;est ce qui m&#39;attire l&#39;opprobre;</p>

<p><sup class="versenum">11&nbsp;</sup>(69:12) Je prends un sac pour v&ecirc;tement, Et je suis l&#39;objet de leurs sarcasmes.</p>

<p><sup class="versenum">12&nbsp;</sup>(69:13) Ceux qui sont assis &agrave; la porte parlent de moi, Et les buveurs de liqueurs fortes me mettent en chansons.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="Button2" type="button" class="collapsible bible">Lire Marc 6:3</button><div class="collapsed" id ="Text2">
<!-- begin bible -->

<p><sup class="versenum">3&nbsp;</sup>N&#39;est-ce pas le charpentier, le fils de Marie, le fr&egrave;re de Jacques, de Joses, de Jude et de Simon? et ses soeurs ne sont-elles pas ici parmi nous? Et il &eacute;tait pour eux une occasion de chute.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

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

<ul>
	<li class="nobreak-final-final">Lisez <span class="popup-link" @click = "popUp('pop1')"> H&eacute;breux 5:8-9</span>.&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">8&nbsp;</sup>a appris, bien qu&#39;il f&ucirc;t Fils, l&#39;ob&eacute;issance par les choses qu&#39;il a souffertes,</p>

	<p><sup class="versenum">9&nbsp;</sup>et qui, apr&egrave;s avoir &eacute;t&eacute; &eacute;lev&eacute; &agrave; la perfection, est devenu pour tous ceux qui lui ob&eacute;issent l&#39;auteur d&#39;un salut &eacute;ternel,</p>
	<!-- end bible --></div>
	Nous n&rsquo;avons pas beaucoup d&rsquo;informations au sujet de l&rsquo;adolescence de J&eacute;sus mais nous pouvons supposer qu&rsquo;il a grandi dans les conditions normales des Juifs. Il &eacute;tait l&rsquo;ain&eacute; d&rsquo;une famille large (<span class="popup-link" @click = "popUp('pop2')"> Marc 6:3</span>).&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">3&nbsp;</sup>N&#39;est-ce pas le charpentier, le fils de Marie, le fr&egrave;re de Jacques, de Joses, de Jude et de Simon? et ses soeurs ne sont-elles pas ici parmi nous? Et il &eacute;tait pour eux une occasion de chute.</p>
	<!-- end bible --></div>
	&nbsp;Il aurait rejoint Joseph pour apprendre le m&eacute;tier de la famille qui est d&rsquo;&ecirc;tre un constructeur. La Bible dit que comme nous, &laquo; Il a appris l&rsquo;ob&eacute;issance &raquo; (<span class="popup-link" @click = "popUp('pop3')"> H&eacute;breux 5:8</span>).&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">8&nbsp;</sup>a appris, bien qu&#39;il f&ucirc;t Fils, l&#39;ob&eacute;issance par les choses qu&#39;il a souffertes,</p>
	<!-- end bible --></div>
	En d&rsquo;autres termes, il a accept&eacute; les corrections et a r&eacute;pondu de fa&ccedil;on appropri&eacute;e. Il a &eacute;t&eacute; insult&eacute; par ses Fr&egrave;res et a &eacute;t&eacute; ignor&eacute; par eux. Apr&egrave;s la mort de Joseph, il serait devenu le pourvoyeur de la famille jusqu&rsquo;&agrave; ce que Son minist&egrave;re publique commence (<span class="popup-link" @click = "popUp('pop4')"> Marc 6:3</span>).&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">3&nbsp;</sup>N&#39;est-ce pas le charpentier, le fils de Marie, le fr&egrave;re de Jacques, de Joses, de Jude et de Simon? et ses soeurs ne sont-elles pas ici parmi nous? Et il &eacute;tait pour eux une occasion de chute.</p>
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

			<td class="social" @click="share('lesson', 'Jésus comme un Jeune Homme et Charpentier/Constructeur: ', '/content/M2/fra/multiply2/multiply205.html')">
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