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
                        <div class="chapter_number ltr"><h1>8.</h1></div>
                        <div class="chapter_title ltr"><h1>Question Fascinante et Soin</h1></div>
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

<p>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</p>

<ul>
	<li>Exemple: <span class="popup-link" @click = "popUp('pop1')"> Psaumes 33:1-5</span>&nbsp;et 1-2 chants

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Justes, r&eacute;jouissez-vous en l&#39;&Eacute;ternel! La louange sied aux hommes droits.</p>

	<p><sup class="versenum">2&nbsp;</sup>C&eacute;l&eacute;brez l&#39;&Eacute;ternel avec la harpe, C&eacute;l&eacute;brez-le sur le luth &agrave; dix cordes.</p>

	<p><sup class="versenum">3&nbsp;</sup>Chantez-lui un cantique nouveau! Faites retentir vos instruments et vos voix!</p>

	<p><sup class="versenum">4&nbsp;</sup>Car la parole de l&#39;&Eacute;ternel est droite, Et toutes ses oeuvres s&#39;accomplissent avec fid&eacute;lit&eacute;;</p>

	<p><sup class="versenum">5&nbsp;</sup>Il aime la justice et la droiture; La bont&eacute; de l&#39;&Eacute;ternel remplit la terre.</p>
	<!-- end bible --></div>
	</li>
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

<p>Encourager l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour</p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

<p>Les premi&egrave;res paroles de J&eacute;sus dans Marc disaient aux gens de se &laquo;repentir.&raquo; Cela signifie changer toute notre fa&ccedil;on de penser parce que les voies de Dieu sont si diff&eacute;rentes des n&ocirc;tres. La fa&ccedil;on dont nous nous voyons en est un domaine. Nous avons besoin d&#39;une nouvelle compr&eacute;hension de la vie avec Dieu et de ce qu&#39;il peut faire dans nos vies. Les paroles suivantes de J&eacute;sus furent &laquo; Suivez-Moi, et Je vous ferai p&ecirc;cheurs d&rsquo;hommes. &raquo; Chaque disciple de J&eacute;sus est appel&eacute; &agrave; vivre ce double appel &agrave; le suivre et &agrave; p&ecirc;cher des hommes. Notre engagement sacrificiel envers J&eacute;sus transforme la vie quotidienne et toutes nos relations. Encourageons-nous &agrave; nous repentir continuellement, &agrave; suivre et &agrave; p&ecirc;cher!</p>

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

<p>Deux semaines avant la mort de J&eacute;sus, Lui et Ses disciples &eacute;taient dans une ville appel&eacute;e J&eacute;richo. Comme ils &eacute;taient partis pour parcourir les 24 km de la montagne jusqu&#39;&agrave; J&eacute;rusalem, un homme aveugle appela J&eacute;sus pour attirer son attention. Cette histoire nous dit ce qui s&rsquo;est pass&eacute; par la suite.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Luc 18:35-43 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 18:35-43</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">35&nbsp;</sup>Comme J&eacute;sus approchait de J&eacute;richo, un aveugle &eacute;tait assis au bord du chemin, et mendiait.</p>

<p><sup class="versenum">36&nbsp;</sup>Entendant la foule passer, il demanda ce que c&#39;&eacute;tait.</p>

<p><sup class="versenum">37&nbsp;</sup>On lui dit: C&#39;est J&eacute;sus de Nazareth qui passe.</p>

<p><sup class="versenum">38&nbsp;</sup>Et il cria: J&eacute;sus, Fils de David, aie piti&eacute; de moi!</p>

<p><sup class="versenum">39&nbsp;</sup>Ceux qui marchaient devant le reprenaient, pour le faire taire; mais il criait beaucoup plus fort: Fils de David, aie piti&eacute; de moi!</p>

<p><sup class="versenum">40&nbsp;</sup>J&eacute;sus, s&#39;&eacute;tant arr&ecirc;t&eacute;, ordonna qu&#39;on le lui am&egrave;ne; et, quand il se fut approch&eacute;,</p>

<p><sup class="versenum">41&nbsp;</sup>il lui demanda: Que veux-tu que je te fasse? Il r&eacute;pondit: Seigneur, que je recouvre la vue.</p>

<p><sup class="versenum">42&nbsp;</sup>Et J&eacute;sus lui dit: Recouvre la vue; ta foi t&#39;a sauv&eacute;.</p>

<p><sup class="versenum">43&nbsp;</sup>A l&#39;instant il recouvra la vue, et suivit J&eacute;sus, en glorifiant Dieu. Tout le peuple, voyant cela, loua Dieu.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/108.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 18:35-43&nbsp; </button>
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
	<li>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<ul>
	<li class="nobreak-final-final">J&eacute;sus a une grande compassion pour les gens! Il a pos&eacute; &agrave; l&#39;aveugle une question fascinante: &laquo;Que veux-tu que je fasse pour toi?&raquo; Puis Il a pourvu aux besoins de l&#39;homme. Dans <span class="popup-link" @click = "popUp('pop2')"> Jean 14: 12-13</span>.&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">12&nbsp;</sup>En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je vous le dis, celui qui croit en moi fera aussi les oeuvres que je fais, et il en fera de plus grandes, parce que je m&#39;en vais au P&egrave;re;</p>

	<p><sup class="versenum">13&nbsp;</sup>et tout ce que vous demanderez en mon nom, je le ferai, afin que le P&egrave;re soit glorifi&eacute; dans le Fils.</p>
	<!-- end bible --></div>
	J&eacute;sus a dit: &laquo; celui qui croit en moi fera aussi les &oelig;uvres que je fais, et il en fera de plus grandes, parce que je m&rsquo;en vais au P&egrave;re ; et tout ce que vous demanderez en mon nom, je le ferai, afin que le P&egrave;re soit glorifi&eacute; dans le Fils. &raquo; En tant que disciples de J&eacute;sus, nous prenons l&#39;initiative de manifester de la compassion aux gens dans la puissance de l&#39;Esprit en leur posant la m&ecirc;me question fascinante et en r&eacute;pondant &agrave; leurs besoins de mani&egrave;re pratique.</li>
</ul>

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
	<li>Entra&icirc;nez-vous &agrave; raconter l&#39;histoire et &agrave; utiliser la question fascinante. Il faut inclure la pratique sur la transition d&#39;une conversation vers l&rsquo;histoire.</li>
	<li>Facultatif: Racontez l&#39;histoire en utilisant l&rsquo;extrait de vid&eacute;o JESUS</li>
	<li>Mettez &agrave; jour votre liste de r&eacute;seau avec des noms de personnes suppl&eacute;mentaires si n&eacute;cessaire.</li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission&nbsp;</h2>

<ul>
	<li>Identifiez 5 personnes de votre Liste de R&eacute;seau avec qui vous pouvez prier et prendre soin en utilisant la Question Fascinante.</li>
	<li>Ecrivez des promesses &laquo; Je le ferai d&rsquo;ici quand &raquo; et partagez avec votre petit groupe.</li>
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


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Question Fascinante et Soin: ', '/content/M2/fra/multiply1/multiply108.html')">
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