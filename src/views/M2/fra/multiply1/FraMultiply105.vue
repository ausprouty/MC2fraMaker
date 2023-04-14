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
                        <div class="chapter_number ltr"><h1>5.</h1></div>
                        <div class="chapter_title ltr"><h1>Grandir dans la Parole de Dieu</h1></div>
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

<p>Lisez un passage biblique, et ex&eacute;cutez un chant pour commencer &agrave; poser les fondements de l&rsquo;adoration et de la louange.</p>

<ul>
	<li>Exemple: Lisez <span class="popup-link" @click = "popUp('pop6')"> Apocalypse 7:12</span>

	<div class="popup invisible" id="pop6"><!-- begin bible -->
	<p><sup class="versenum">12&nbsp;</sup>en disant: Amen! La louange, la gloire, la sagesse, l&#39;action de gr&acirc;ces, l&#39;honneur, la puissance, et la force, soient &agrave; notre Dieu, aux si&egrave;cles des si&egrave;cles! Amen!</p>
	<!-- end bible --></div>
	&laquo; en disant: Amen! La louange, la gloire, la sagesse, l&rsquo;action de gr&acirc;ces, l&rsquo;honneur, la puissance, et la force, soient &agrave; notre Dieu, aux si&egrave;cles des si&egrave;cles, Amen! &raquo;</li>
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

<ul>
	<li class="nobreak-final-final">Exemple: Dieu nous a fait don de toute b&eacute;n&eacute;diction spirituelle &agrave; travers J&eacute;sus. Il nous a adopt&eacute;s dans sa famille et nous a appel&eacute;s Ses Enfants. &laquo; En Lui, vous aussi, apr&egrave;s avoir entendu la parole de la v&eacute;rit&eacute;, l&rsquo;Evangile de votre salut, en lui vous avez cru et vous avez &eacute;t&eacute; scell&eacute;s du Saint Esprit qui avait &eacute;t&eacute; promis, lequel est un gage de notre h&eacute;ritage &raquo; <span class="popup-link" @click = "popUp('pop7')"> &Eacute;ph&eacute;siens 1:13-14</span>.&nbsp;

	<div class="popup invisible" id="pop7"><!-- begin bible -->
	<p><sup class="versenum">13&nbsp;</sup>En lui vous aussi, apr&egrave;s avoir entendu la parole de la v&eacute;rit&eacute;, l&#39;&Eacute;vangile de votre salut, en lui vous avez cru et vous avez &eacute;t&eacute; scell&eacute;s du Saint Esprit qui avait &eacute;t&eacute; promis,</p>

	<p><sup class="versenum">14&nbsp;</sup>lequel est un gage de notre h&eacute;ritage, pour la r&eacute;demption de ceux que Dieu s&#39;est acquis, &agrave; la louange de sa gloire.</p>
	<!-- end bible --></div>
	</li>
</ul>
&nbsp;Quel don merveilleux! C&rsquo;est la promesse de Dieu pour vous.

</div>
</div>

<div class="up">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<h2>Contexte</h2>

<p>Apr&egrave;s que J&eacute;sus fut ressuscit&eacute;, il apparut plusieurs fois &agrave; ses disciples pendant une p&eacute;riode de 40 jours. Un jour, il leur apparut alors qu&rsquo;ils s&rsquo;&eacute;taient rassembl&eacute;s dans une grande salle, et il leur expliqua l&rsquo;importance de sa Parole</p>

<h2>Lire</h2>

<p>Lisez ou observez Luc 24:36-49 deux fois pendant que tout le monde &eacute;coute</p>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 24:36-49</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">36&nbsp;</sup>Tandis qu&#39;ils parlaient de la sorte, lui-m&ecirc;me se pr&eacute;senta au milieu d&#39;eux, et leur dit: La paix soit avec vous!</p>

<p><sup class="versenum">37&nbsp;</sup>Saisis de frayeur et d&#39;&eacute;pouvante, ils croyaient voir un esprit.</p>

<p><sup class="versenum">38&nbsp;</sup>Mais il leur dit: Pourquoi &ecirc;tes-vous troubl&eacute;s, et pourquoi pareilles pens&eacute;es s&#39;&eacute;l&egrave;vent-elles dans vos coeurs?</p>

<p><sup class="versenum">39&nbsp;</sup>Voyez mes mains et mes pieds, c&#39;est bien moi; touchez-moi et voyez: un esprit n&#39;a ni chair ni os, comme vous voyez que j&#39;ai.</p>

<p><sup class="versenum">40&nbsp;</sup>Et en disant cela, il leur montra ses mains et ses pieds.</p>

<p><sup class="versenum">41&nbsp;</sup>Comme, dans leur joie, ils ne croyaient point encore, et qu&#39;ils &eacute;taient dans l&#39;&eacute;tonnement, il leur dit: Avez-vous ici quelque chose &agrave; manger?</p>

<p><sup class="versenum">42&nbsp;</sup>Ils lui pr&eacute;sent&egrave;rent du poisson r&ocirc;ti et un rayon de miel.</p>

<p><sup class="versenum">43&nbsp;</sup>Il en prit, et il mangea devant eux.</p>

<p><sup class="versenum">44&nbsp;</sup>Puis il leur dit: C&#39;est l&agrave; ce que je vous disais lorsque j&#39;&eacute;tais encore avec vous, qu&#39;il fallait que s&#39;accompl&icirc;t tout ce qui est &eacute;crit de moi dans la loi de Mo&iuml;se, dans les proph&egrave;tes, et dans les psaumes.</p>

<p><sup class="versenum">45&nbsp;</sup>Alors il leur ouvrit l&#39;esprit, afin qu&#39;ils comprissent les &Eacute;critures.</p>

<p><sup class="versenum">46&nbsp;</sup>Et il leur dit: Ainsi il est &eacute;crit que le Christ souffrirait, et qu&#39;il ressusciterait des morts le troisi&egrave;me jour,</p>

<p><sup class="versenum">47&nbsp;</sup>et que la repentance et le pardon des p&eacute;ch&eacute;s seraient pr&ecirc;ch&eacute;s en son nom &agrave; toutes les nations, &agrave; commencer par J&eacute;rusalem.</p>

<p><sup class="versenum">48&nbsp;</sup>Vous &ecirc;tes t&eacute;moins de ces choses.</p>

<p><sup class="versenum">49&nbsp;</sup>Et voici, j&#39;enverrai sur vous ce que mon P&egrave;re a promis; mais vous, restez dans la ville jusqu&#39;&agrave; ce que vous soyez rev&ecirc;tus de la puissance d&#39;en haut.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/105.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 24:36-49&nbsp; </button>
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
<div id="Summary2" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<p>J&eacute;sus veut que nous comprenions la parole de Dieu et ce qu&rsquo;elle nous enseigne par rapport &agrave; Lui. La vie de J&eacute;sus a accompli les promesses faites dans la Parole de Dieu. Il veut que nous parlions de ce que nous avons appris aux autres.</p>

<ul>
	<li class="nobreak-final-final">Lisez <span class="popup-link" @click = "popUp('pop3')"> 2 Timoth&eacute;e 3:16-17</span>,&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">16&nbsp;</sup>Toute &Eacute;criture est inspir&eacute;e de Dieu, et utile pour enseigner, pour convaincre, pour corriger, pour instruire dans la justice,</p>

	<p><sup class="versenum">17&nbsp;</sup>afin que l&#39;homme de Dieu soit accompli et propre &agrave; toute bonne oeuvre.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop4')"> Romains 10:17</span>

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">17&nbsp;</sup>Ainsi la foi vient de ce qu&#39;on entend, et ce qu&#39;on entend vient de la parole de Christ.</p>
	<!-- end bible --></div>
	et <span class="popup-link" @click = "popUp('pop5')"> H&eacute;breux 4:12</span>

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">12&nbsp;</sup>Car la parole de Dieu est vivante et efficace, plus tranchante qu&#39;une &eacute;p&eacute;e quelconque &agrave; deux tranchants, p&eacute;n&eacute;trante jusqu&#39;&agrave; partager &acirc;me et esprit, jointures et moelles; elle juge les sentiments et les pens&eacute;es du coeur.</p>
	<!-- end bible --></div>
	pour mettre en &eacute;vidence les v&eacute;rit&eacute;s concernant la parole de Dieu.</li>
</ul>

<p>Lire la Bible chaque jour est &eacute;l&eacute;ment d&eacute;terminant pour apprendre &agrave; connaitre J&eacute;sus</p>

</div>
</div>

<div class="forward">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ Se Pr&eacute;parer pour la Mission</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<ul>
	<li>Prenez l&rsquo;engagement de lire au moins un chapitre dans la Parole de Dieu chaque jour en commen&ccedil;ant par l&rsquo;Evangile de Jean.</li>
	<li>Priez afin que l&rsquo;Esprit Saint vous enseigne &agrave; travers Sa Parole, lisez le chapitre et r&eacute;pondez aux trois questions ci-apr&egrave;s:
	<ul>
		<li>De quoi parle ce passage?</li>
		<li>Comment puis-je l&rsquo;appliquer?</li>
		<li>Qui puis-je aider avec ce passage?</li>
	</ul>
	</li>
	<li>M&eacute;ditez sur ce que l&rsquo;Esprit Saint vous a enseign&eacute; &agrave; travers ce passage.</li>
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
	<li>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser pour initier un mouvement de faiseurs de disciples.</li>
</ul>
</div>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Grandir dans la Parole de Dieu: ', '/content/M2/fra/multiply1/multiply105.html')">
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