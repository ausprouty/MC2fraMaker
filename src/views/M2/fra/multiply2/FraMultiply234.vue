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
                        <div class="chapter_number ltr"><h1>34.</h1></div>
                        <div class="chapter_title ltr"><h1>Envoie des Leaders</h1></div>
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
	<li>Lisez ou observez Luc 9:1-6; Matthieu 10:5-23 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 9:1-6</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>J&eacute;sus, ayant assembl&eacute; les douze, leur donna force et pouvoir sur tous les d&eacute;mons, avec la puissance de gu&eacute;rir les maladies.</p>

<p><sup class="versenum">2&nbsp;</sup>Il les envoya pr&ecirc;cher le royaume de Dieu, et gu&eacute;rir les malades.</p>

<p><sup class="versenum">3&nbsp;</sup>Ne prenez rien pour le voyage, leur dit-il, ni b&acirc;ton, ni sac, ni pain, ni argent, et n&#39;ayez pas deux tuniques.</p>

<p><sup class="versenum">4&nbsp;</sup>Dans quelque maison que vous entriez, restez-y; et c&#39;est de l&agrave; que vous partirez.</p>

<p><sup class="versenum">5&nbsp;</sup>Et, si les gens ne vous re&ccedil;oivent pas, sortez de cette ville, et secouez la poussi&egrave;re de vos pieds, en t&eacute;moignage contre eux.</p>

<p><sup class="versenum">6&nbsp;</sup>Ils partirent, et ils all&egrave;rent de village en village, annon&ccedil;ant la bonne nouvelle et op&eacute;rant partout des gu&eacute;risons.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/234.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 9:1-6&nbsp; </button>
    <div class="collapsed"></div>

<button id="Button1" type="button" class="collapsible bible">Lire Matthieu 10:5-23</button><div class="collapsed" id ="Text1">
<!-- begin bible -->

<p><sup class="versenum">5&nbsp;</sup>Tels sont les douze que J&eacute;sus envoya, apr&egrave;s leur avoir donn&eacute; les instructions suivantes: N&#39;allez pas vers les pa&iuml;ens, et n&#39;entrez pas dans les villes des Samaritains;</p>

<p><sup class="versenum">6&nbsp;</sup>allez plut&ocirc;t vers les brebis perdues de la maison d&#39;Isra&euml;l.</p>

<p><sup class="versenum">7&nbsp;</sup>Allez, pr&ecirc;chez, et dites: Le royaume des cieux est proche.</p>

<p><sup class="versenum">8&nbsp;</sup>Gu&eacute;rissez les malades, ressuscitez les morts, purifiez les l&eacute;preux, chassez les d&eacute;mons. Vous avez re&ccedil;u gratuitement, donnez gratuitement.</p>

<p><sup class="versenum">9&nbsp;</sup>Ne prenez ni or, ni argent, ni monnaie, dans vos ceintures;</p>

<p><sup class="versenum">10&nbsp;</sup>ni sac pour le voyage, ni deux tuniques, ni souliers, ni b&acirc;ton; car l&#39;ouvrier m&eacute;rite sa nourriture.</p>

<p><sup class="versenum">11&nbsp;</sup>Dans quelque ville ou village que vous entriez, informez-vous s&#39;il s&#39;y trouve quelque homme digne de vous recevoir; et demeurez chez lui jusqu&#39;&agrave; ce que vous partiez.</p>

<p><sup class="versenum">12&nbsp;</sup>En entrant dans la maison, saluez-la;</p>

<p><sup class="versenum">13&nbsp;</sup>et, si la maison en est digne, que votre paix vienne sur elle; mais si elle n&#39;en est pas digne, que votre paix retourne &agrave; vous.</p>

<p><sup class="versenum">14&nbsp;</sup>Lorsqu&#39;on ne vous recevra pas et qu&#39;on n&#39;&eacute;coutera pas vos paroles, sortez de cette maison ou de cette ville et secouez la poussi&egrave;re de vos pieds.</p>

<p><sup class="versenum">15&nbsp;</sup>Je vous le dis en v&eacute;rit&eacute;: au jour du jugement, le pays de Sodome et de Gomorrhe sera trait&eacute; moins rigoureusement que cette ville-l&agrave;.</p>

<p><sup class="versenum">16&nbsp;</sup>Voici, je vous envoie comme des brebis au milieu des loups. Soyez donc prudents comme les serpents, et simples comme les colombes.</p>

<p><sup class="versenum">17&nbsp;</sup>Mettez-vous en garde contre les hommes; car ils vous livreront aux tribunaux, et ils vous battront de verges dans leurs synagogues;</p>

<p><sup class="versenum">18&nbsp;</sup>vous serez men&eacute;s, &agrave; cause de moi, devant des gouverneurs et devant des rois, pour servir de t&eacute;moignage &agrave; eux et aux pa&iuml;ens.</p>

<p><sup class="versenum">19&nbsp;</sup>Mais, quand on vous livrera, ne vous inqui&eacute;tez ni de la mani&egrave;re dont vous parlerez ni de ce que vous direz: ce que vous aurez &agrave; dire vous sera donn&eacute; &agrave; l&#39;heure m&ecirc;me;</p>

<p><sup class="versenum">20&nbsp;</sup>car ce n&#39;est pas vous qui parlerez, c&#39;est l&#39;Esprit de votre P&egrave;re qui parlera en vous.</p>

<p><sup class="versenum">21&nbsp;</sup>Le fr&egrave;re livrera son fr&egrave;re &agrave; la mort, et le p&egrave;re son enfant; les enfants se soul&egrave;veront contre leurs parents, et les feront mourir.</p>

<p><sup class="versenum">22&nbsp;</sup>Vous serez ha&iuml;s de tous, &agrave; cause de mon nom; mais celui qui pers&eacute;v&eacute;rera jusqu&#39;&agrave; la fin sera sauv&eacute;.</p>

<p><sup class="versenum">23&nbsp;</sup>Quand on vous pers&eacute;cutera dans une ville, fuyez dans une autre. Je vous le dis en v&eacute;rit&eacute;, vous n&#39;aurez pas achev&eacute; de parcourir les villes d&#39;Isra&euml;l que le Fils de l&#39;homme sera venu.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/234-1.mp4" type="button" class="external-movie">
         Regardez &nbsp;Matthieu 10:5-23&nbsp; </button>
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

<p>Apr&egrave;s des mois de formation au minist&egrave;re, les leaders sont pr&ecirc;ts &agrave; &ecirc;tre envoy&eacute;s par leurs propres moyens. Rappelez-vous qu&#39;ils ont &eacute;t&eacute; d&eacute;sign&eacute;s en tant que leaders afin qu&#39;ils puissent &ecirc;tre avec Lui et qu&#39;Il puisse les envoyer pour faire les m&ecirc;mes choses qu&#39;Il faisait. Avant de les envoyer en &eacute;quipe de deux, il a donn&eacute; des instructions claires sur ce qu&#39;il fallait faire, quoi dire, combien de temps rester, et comment r&eacute;agir quand ils sont pers&eacute;cut&eacute;s. Il les a envoy&eacute;s comme le P&egrave;re l&#39;avait envoy&eacute; dans le monde, dans une d&eacute;pendance compl&egrave;te de Dieu pour tout ce dont ils auraient besoin. Cette mission &agrave; court terme &eacute;tait dans leur propre pays, envers des gens qui leur ressemblaient et parlaient leur langue. C&rsquo;est pour la premi&egrave;re fois qu&rsquo;ils sont envoy&eacute;s faire le minist&egrave;re sans que J&eacute;sus soit avec eux. Ce qui avait &eacute;t&eacute; une seule &eacute;quipe de J&eacute;sus avec les Douze est maintenant restructur&eacute; en sept &eacute;quipes, six &eacute;quipes de deux et J&eacute;sus qui continue avec d&rsquo;autres dans la formation.</p>

<ul>
	<li>Pour une &eacute;tude approfondie <span class="popup-link" @click = "popUp('pop1')"> Marc 6:7-13</span>.

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">7&nbsp;</sup>Alors il appela les douze, et il commen&ccedil;a &agrave; les envoyer deux &agrave; deux, en leur donnant pouvoir sur les esprits impurs.</p>

	<p><sup class="versenum">8&nbsp;</sup>Il leur prescrivit de ne rien prendre pour le voyage, si ce n&#39;est un b&acirc;ton; de n&#39;avoir ni pain, ni sac, ni monnaie dans la ceinture;</p>

	<p><sup class="versenum">9&nbsp;</sup>de chausser des sandales, et de ne pas rev&ecirc;tir deux tuniques.</p>

	<p><sup class="versenum">10&nbsp;</sup>Puis il leur dit: Dans quelque maison que vous entriez, restez-y jusqu&#39;&agrave; ce que vous partiez de ce lieu.</p>

	<p><sup class="versenum">11&nbsp;</sup>Et, s&#39;il y a quelque part des gens qui ne vous re&ccedil;oivent ni ne vous &eacute;coutent, retirez-vous de l&agrave;, et secouez la poussi&egrave;re de vos pieds, afin que cela leur serve de t&eacute;moignage.</p>

	<p><sup class="versenum">12&nbsp;</sup>Ils partirent, et ils pr&ecirc;ch&egrave;rent la repentance.</p>

	<p><sup class="versenum">13&nbsp;</sup>Ils chassaient beaucoup de d&eacute;mons, et ils oignaient d&#39;huile beaucoup de malades et les gu&eacute;rissaient.</p>
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

			<td class="social" @click="share('lesson', 'Envoie des Leaders: ', '/content/M2/fra/multiply2/multiply234.html')">
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