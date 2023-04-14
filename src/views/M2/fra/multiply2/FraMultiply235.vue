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
                        <div class="chapter_number ltr"><h1>35.</h1></div>
                        <div class="chapter_title ltr"><h1>Diriger pendant le deuil</h1></div>
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
	<li>Lisez ou observez Matthieu 14:1-14; Marc 6:30 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Matthieu 14:1-14</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>En ce temps-l&agrave;, H&eacute;rode le t&eacute;trarque, ayant entendu parler de J&eacute;sus, dit &agrave; ses serviteurs: C&#39;est Jean Baptiste!</p>

<p><sup class="versenum">2&nbsp;</sup>Il est ressuscit&eacute; des morts, et c&#39;est pour cela qu&#39;il se fait par lui des miracles.</p>

<p><sup class="versenum">3&nbsp;</sup>Car H&eacute;rode, qui avait fait arr&ecirc;ter Jean, l&#39;avait li&eacute; et mis en prison, &agrave; cause d&#39;H&eacute;rodias, femme de Philippe, son fr&egrave;re,</p>

<p><sup class="versenum">4&nbsp;</sup>parce que Jean lui disait: Il ne t&#39;est pas permis de l&#39;avoir pour femme.</p>

<p><sup class="versenum">5&nbsp;</sup>Il voulait le faire mourir, mais il craignait la foule, parce qu&#39;elle regardait Jean comme un proph&egrave;te.</p>

<p><sup class="versenum">6&nbsp;</sup>Or, lorsqu&#39;on c&eacute;l&eacute;bra l&#39;anniversaire de la naissance d&#39;H&eacute;rode, la fille d&#39;H&eacute;rodias dansa au milieu des convives, et plut &agrave; H&eacute;rode,</p>

<p><sup class="versenum">7&nbsp;</sup>de sorte qu&#39;il promit avec serment de lui donner ce qu&#39;elle demanderait.</p>

<p><sup class="versenum">8&nbsp;</sup>A l&#39;instigation de sa m&egrave;re, elle dit: Donne-moi ici, sur un plat, la t&ecirc;te de Jean Baptiste.</p>

<p><sup class="versenum">9&nbsp;</sup>Le roi fut attrist&eacute;; mais, &agrave; cause de ses serments et des convives, il commanda qu&#39;on la lui donne,</p>

<p><sup class="versenum">10&nbsp;</sup>et il envoya d&eacute;capiter Jean dans la prison.</p>

<p><sup class="versenum">11&nbsp;</sup>Sa t&ecirc;te fut apport&eacute;e sur un plat, et donn&eacute;e &agrave; la jeune fille, qui la porta &agrave; sa m&egrave;re.</p>

<p><sup class="versenum">12&nbsp;</sup>Les disciples de Jean vinrent prendre son corps, et l&#39;ensevelirent. Et ils all&egrave;rent l&#39;annoncer &agrave; J&eacute;sus.</p>

<p><sup class="versenum">13&nbsp;</sup>A cette nouvelle, J&eacute;sus partit de l&agrave; dans une barque, pour se retirer &agrave; l&#39;&eacute;cart dans un lieu d&eacute;sert; et la foule, l&#39;ayant su, sortit des villes et le suivit &agrave; pied.</p>

<p><sup class="versenum">14&nbsp;</sup>Quand il sortit de la barque, il vit une grande foule, et fut &eacute;mu de compassion pour elle, et il gu&eacute;rit les malades.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/235.mp4" type="button" class="external-movie">
         Regardez &nbsp;Matthieu 14:1-14&nbsp; </button>
    <div class="collapsed"></div>

<button id="Button1" type="button" class="collapsible bible">Lire Marc 6:30</button><div class="collapsed" id ="Text1">
<!-- begin bible -->

<p><sup class="versenum">30&nbsp;</sup>Les ap&ocirc;tres, s&#39;&eacute;tant rassembl&eacute;s aupr&egrave;s de J&eacute;sus, lui racont&egrave;rent tout ce qu&#39;ils avaient fait et tout ce qu&#39;ils avaient enseign&eacute;.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/235-1.mp4" type="button" class="external-movie">
         Regardez &nbsp;Marc 6:30&nbsp; </button>
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

<p>Pendant que les ap&ocirc;tres &eacute;taient en voyage pour leur minist&egrave;re, le roi H&eacute;rode Antipas c&eacute;l&eacute;brait son anniversaire. Il a organis&eacute; un grand banquet et a invit&eacute; tous les commandants militaires et les gens de la haute soci&eacute;t&eacute; de Galil&eacute;e &agrave; l&#39;un de ses palais. Il a fait une promesse folle &agrave; sa ni&egrave;ce parce qu&#39;il aimait la fa&ccedil;on dont elle dansait pour les invit&eacute;s. Elle a demand&eacute; &agrave; sa m&egrave;re qui a saisi l&#39;occasion de se venger de Jean-Baptiste. Elle a demand&eacute; sa d&eacute;capitation. H&eacute;rode, ne voulant pas perdre la face devant ses invit&eacute;s, ob&eacute;it et Jean fut ex&eacute;cut&eacute;. J&eacute;sus continuait Sa formation et Son discip&ocirc;lat envers d&rsquo;autres pendant qu&#39;il voyageait de ville en ville (Matthieu 11: 1). La nouvelle de la mort de Jean parvint &agrave; J&eacute;sus au moment m&ecirc;me o&ugrave; les ap&ocirc;tres revenaient de leurs voyages missionnaires. J&eacute;sus a &eacute;t&eacute; attrist&eacute; par la mort de Jean et a voulu &ecirc;tre avec ses plus proches leaders. Ils ont alors essay&eacute; de trouver une place pour une retraite. Il mod&eacute;lisait comment diriger pendant les p&eacute;riodes de deuil et d&#39;&eacute;puisement.</p>

<ul>
	<li class="nobreak-final-final">Pour une &eacute;tude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Marc 6:14-34</span>;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">14&nbsp;</sup>Le roi H&eacute;rode entendit parler de J&eacute;sus, dont le nom &eacute;tait devenu c&eacute;l&egrave;bre, et il dit: Jean Baptiste est ressuscit&eacute; des morts, et c&#39;est pour cela qu&#39;il se fait par lui des miracles.</p>

	<p><sup class="versenum">15&nbsp;</sup>D&#39;autres disaient: C&#39;est &Eacute;lie. Et d&#39;autres disaient: C&#39;est un proph&egrave;te comme l&#39;un des proph&egrave;tes.</p>

	<p><sup class="versenum">16&nbsp;</sup>Mais H&eacute;rode, en apprenant cela, disait: Ce Jean que j&#39;ai fait d&eacute;capiter, c&#39;est lui qui est ressuscit&eacute;.</p>

	<p><sup class="versenum">17&nbsp;</sup>Car H&eacute;rode lui-m&ecirc;me avait fait arr&ecirc;ter Jean, et l&#39;avait fait lier en prison, &agrave; cause d&#39;H&eacute;rodias, femme de Philippe, son fr&egrave;re, parce qu&#39;il l&#39;avait &eacute;pous&eacute;e,</p>

	<p><sup class="versenum">18&nbsp;</sup>et que Jean lui disait: Il ne t&#39;est pas permis d&#39;avoir la femme de ton fr&egrave;re.</p>

	<p><sup class="versenum">19&nbsp;</sup>H&eacute;rodias &eacute;tait irrit&eacute;e contre Jean, et voulait le faire mourir.</p>

	<p><sup class="versenum">20&nbsp;</sup>Mais elle ne le pouvait; car H&eacute;rode craignait Jean, le connaissant pour un homme juste et saint; il le prot&eacute;geait, et, apr&egrave;s l&#39;avoir entendu, il &eacute;tait souvent perplexe, et l&#39;&eacute;coutait avec plaisir.</p>

	<p><sup class="versenum">21&nbsp;</sup>Cependant, un jour propice arriva, lorsque H&eacute;rode, &agrave; l&#39;anniversaire de sa naissance, donna un festin &agrave; ses grands, aux chefs militaires et aux principaux de la Galil&eacute;e.</p>

	<p><sup class="versenum">22&nbsp;</sup>La fille d&#39;H&eacute;rodias entra dans la salle; elle dansa, et plut &agrave; H&eacute;rode et &agrave; ses convives. Le roi dit &agrave; la jeune fille: Demande-moi ce que tu voudras, et je te le donnerai.</p>

	<p><sup class="versenum">23&nbsp;</sup>Il ajouta avec serment: Ce que tu me demanderas, je te le donnerai, f&ucirc;t-ce la moiti&eacute; de mon royaume.</p>

	<p><sup class="versenum">24&nbsp;</sup>&Eacute;tant sortie, elle dit &agrave; sa m&egrave;re: Que demanderais-je? Et sa m&egrave;re r&eacute;pondit: La t&ecirc;te de Jean Baptiste.</p>

	<p><sup class="versenum">25&nbsp;</sup>Elle s&#39;empressa de rentrer aussit&ocirc;t vers le roi, et lui fit cette demande: Je veux que tu me donnes &agrave; l&#39;instant, sur un plat, la t&ecirc;te de Jean Baptiste.</p>

	<p><sup class="versenum">26&nbsp;</sup>Le roi fut attrist&eacute;; mais, &agrave; cause de ses serments et des convives, il ne voulut pas lui faire un refus.</p>

	<p><sup class="versenum">27&nbsp;</sup>Il envoya sur-le-champ un garde, avec ordre d&#39;apporter la t&ecirc;te de Jean Baptiste.</p>

	<p><sup class="versenum">28&nbsp;</sup>Le garde alla d&eacute;capiter Jean dans la prison, et apporta la t&ecirc;te sur un plat. Il la donna &agrave; la jeune fille, et la jeune fille la donna &agrave; sa m&egrave;re.</p>

	<p><sup class="versenum">29&nbsp;</sup>Les disciples de Jean, ayant appris cela, vinrent prendre son corps, et le mirent dans un s&eacute;pulcre.</p>

	<p><sup class="versenum">30&nbsp;</sup>Les ap&ocirc;tres, s&#39;&eacute;tant rassembl&eacute;s aupr&egrave;s de J&eacute;sus, lui racont&egrave;rent tout ce qu&#39;ils avaient fait et tout ce qu&#39;ils avaient enseign&eacute;.</p>

	<p><sup class="versenum">31&nbsp;</sup>J&eacute;sus leur dit: Venez &agrave; l&#39;&eacute;cart dans un lieu d&eacute;sert, et reposez-vous un peu. Car il y avait beaucoup d&#39;allants et de venants, et ils n&#39;avaient m&ecirc;me pas le temps de manger.</p>

	<p><sup class="versenum">32&nbsp;</sup>Ils partirent donc dans une barque, pour aller &agrave; l&#39;&eacute;cart dans un lieu d&eacute;sert.</p>

	<p><sup class="versenum">33&nbsp;</sup>Beaucoup de gens les virent s&#39;en aller et les reconnurent, et de toutes les villes on accourut &agrave; pied et on les devan&ccedil;a au lieu o&ugrave; ils se rendaient.</p>

	<p><sup class="versenum">34&nbsp;</sup>Quand il sortit de la barque, J&eacute;sus vit une grande foule, et fut &eacute;mu de compassion pour eux, parce qu&#39;ils &eacute;taient comme des brebis qui n&#39;ont point de berger; et il se mit &agrave; leur enseigner beaucoup de choses.</p>
	<!-- end bible --></div>
	&nbsp;<span class="popup-link" @click = "popUp('pop2')"> Luc 9:7-11</span>.

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">7&nbsp;</sup>H&eacute;rode le t&eacute;trarque entendit parler de tout ce qui se passait, et il ne savait que penser. Car les uns disaient que Jean &eacute;tait ressuscit&eacute; des morts;</p>

	<p><sup class="versenum">8&nbsp;</sup>d&#39;autres, qu&#39;&Eacute;lie &eacute;tait apparu; et d&#39;autres, qu&#39;un des anciens proph&egrave;tes &eacute;tait ressuscit&eacute;.</p>

	<p><sup class="versenum">9&nbsp;</sup>Mais H&eacute;rode disait: J&#39;ai fait d&eacute;capiter Jean; qui donc est celui-ci, dont j&#39;entends dire de telles choses? Et il cherchait &agrave; le voir.</p>

	<p><sup class="versenum">10&nbsp;</sup>Les ap&ocirc;tres, &eacute;tant de retour, racont&egrave;rent &agrave; J&eacute;sus tout ce qu&#39;ils avaient fait. Il les prit avec lui, et se retira &agrave; l&#39;&eacute;cart, du c&ocirc;t&eacute; d&#39;une ville appel&eacute;e Bethsa&iuml;da.</p>

	<p><sup class="versenum">11&nbsp;</sup>Les foules, l&#39;ayant su, le suivirent. J&eacute;sus les accueillit, et il leur parlait du royaume de Dieu; il gu&eacute;rit aussi ceux qui avaient besoin d&#39;&ecirc;tre gu&eacute;ris.</p>
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

			<td class="social" @click="share('lesson', 'Diriger pendant le deuil: ', '/content/M2/fra/multiply2/multiply235.html')">
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