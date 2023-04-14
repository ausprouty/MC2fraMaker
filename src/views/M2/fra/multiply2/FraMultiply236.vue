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
                        <div class="chapter_number ltr"><h1>36.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership et Provision</h1></div>
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
	<li>Lisez ou observez Jean 6:1-14 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 6:1-14</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Apr&egrave;s cela, J&eacute;sus s&#39;en alla de l&#39;autre c&ocirc;t&eacute; de la mer de Galil&eacute;e, de Tib&eacute;riade.</p>

<p><sup class="versenum">2&nbsp;</sup>Une grande foule le suivait, parce qu&#39;elle voyait les miracles qu&#39;il op&eacute;rait sur les malades.</p>

<p><sup class="versenum">3&nbsp;</sup>J&eacute;sus monta sur la montagne, et l&agrave; il s&#39;assit avec ses disciples.</p>

<p><sup class="versenum">4&nbsp;</sup>Or, la P&acirc;que &eacute;tait proche, la f&ecirc;te des Juifs.</p>

<p><sup class="versenum">5&nbsp;</sup>Ayant lev&eacute; les yeux, et voyant qu&#39;une grande foule venait &agrave; lui, J&eacute;sus dit &agrave; Philippe: O&ugrave; ach&egrave;terons-nous des pains, pour que ces gens aient &agrave; manger?</p>

<p><sup class="versenum">6&nbsp;</sup>Il disait cela pour l&#39;&eacute;prouver, car il savait ce qu&#39;il allait faire.</p>

<p><sup class="versenum">7&nbsp;</sup>Philippe lui r&eacute;pondit: Les pains qu&#39;on aurait pour deux cents deniers ne suffiraient pas pour que chacun en re&ccedil;&ucirc;t un peu.</p>

<p><sup class="versenum">8&nbsp;</sup>Un de ses disciples, Andr&eacute;, fr&egrave;re de Simon Pierre, lui dit:</p>

<p><sup class="versenum">9&nbsp;</sup>Il y a ici un jeune gar&ccedil;on qui a cinq pains d&#39;orge et deux poissons; mais qu&#39;est-ce que cela pour tant de gens?</p>

<p><sup class="versenum">10&nbsp;</sup>J&eacute;sus dit: Faites-les asseoir. Il y avait dans ce lieu beaucoup d&#39;herbe. Ils s&#39;assirent donc, au nombre d&#39;environ cinq mille hommes.</p>

<p><sup class="versenum">11&nbsp;</sup>J&eacute;sus prit les pains, rendit gr&acirc;ces, et les distribua &agrave; ceux qui &eacute;taient assis; il leur donna de m&ecirc;me des poissons, autant qu&#39;ils en voulurent.</p>

<p><sup class="versenum">12&nbsp;</sup>Lorsqu&#39;ils furent rassasi&eacute;s, il dit &agrave; ses disciples: Ramassez les morceaux qui restent, afin que rien ne se perde.</p>

<p><sup class="versenum">13&nbsp;</sup>Ils les ramass&egrave;rent donc, et ils remplirent douze paniers avec les morceaux qui rest&egrave;rent des cinq pains d&#39;orge, apr&egrave;s que tous eurent mang&eacute;.</p>

<p><sup class="versenum">14&nbsp;</sup>Ces gens, ayant vu le miracle que J&eacute;sus avait fait, disaient: Celui-ci est vraiment le proph&egrave;te qui doit venir dans le monde.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/236.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 6:1-14&nbsp; </button>
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

<p>J&eacute;sus cherchait un endroit o&ugrave; se retirer avec ses leaders, mais le P&egrave;re avait des plans diff&eacute;rents. Alors qu&#39;ils s&#39;approchent du rivage, J&eacute;sus pouvait d&eacute;j&agrave; voir de grandes foules se rassembler parce qu&#39;ils ont vu les miracles que J&eacute;sus a faits. J&eacute;sus est &eacute;mu de compassion pour eux parce qu&#39;ils ressemblaient &agrave; des brebis sans berger. J&eacute;sus commence &agrave; enseigner la foule immense de 5 000 hommes, plus les femmes et les enfants. J&eacute;sus utilise la situation pour enseigner &agrave; Ses leaders la multiplication et la provision de Dieu en les mettant au d&eacute;fi de donner de la nourriture &agrave; la foule. Ils ont appris:</p>

<ol>
	<li>&agrave; lever les yeux et &agrave; voir le besoin;</li>
	<li>&agrave; permettre &agrave; leurs c&oelig;urs d&#39;&ecirc;tre &eacute;mus de compassion;</li>
	<li>&agrave; rassembler les ressources qu&#39;ils avaient autour d&#39;eux, quelqu&#39;un devrait tout donner pour voir la multiplication se produire;</li>
	<li>&agrave; s&#39;organiser et voir le surnaturel se produire; d&#39;offrir tout ce qu&#39;ils ont &agrave; Dieu dans la foi avec action de gr&acirc;ces</li>
</ol>

<ul>
	<li class="nobreak-final-final">Pour une &eacute;tude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Luc 9:12-17</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">12&nbsp;</sup>Comme le jour commen&ccedil;ait &agrave; baisser, les douze s&#39;approch&egrave;rent, et lui dirent: Renvoie la foule, afin qu&#39;elle aille dans les villages et dans les campagnes des environs, pour se loger et pour trouver des vivres; car nous sommes ici dans un lieu d&eacute;sert.</p>

	<p><sup class="versenum">13&nbsp;</sup>J&eacute;sus leur dit: Donnez-leur vous-m&ecirc;mes &agrave; manger. Mais ils r&eacute;pondirent: Nous n&#39;avons que cinq pains et deux poissons, &agrave; moins que nous n&#39;allions nous-m&ecirc;mes acheter des vivres pour tout ce peuple.</p>

	<p><sup class="versenum">14&nbsp;</sup>Or, il y avait environ cinq mille hommes. J&eacute;sus dit &agrave; ses disciples: Faites-les asseoir par rang&eacute;es de cinquante.</p>

	<p><sup class="versenum">15&nbsp;</sup>Ils firent ainsi, ils les firent tous asseoir.</p>

	<p><sup class="versenum">16&nbsp;</sup>J&eacute;sus prit les cinq pains et les deux poissons, et, levant les yeux vers le ciel, il les b&eacute;nit. Puis, il les rompit, et les donna aux disciples, afin qu&#39;ils les distribuassent &agrave; la foule.</p>

	<p><sup class="versenum">17&nbsp;</sup>Tous mang&egrave;rent et furent rassasi&eacute;s, et l&#39;on emporta douze paniers pleins des morceaux qui restaient.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> Matthieu 14:15-21</span>;&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">15&nbsp;</sup>Le soir &eacute;tant venu, les disciples s&#39;approch&egrave;rent de lui, et dirent: Ce lieu est d&eacute;sert, et l&#39;heure est d&eacute;j&agrave; avanc&eacute;e; renvoie la foule, afin qu&#39;elle aille dans les villages, pour s&#39;acheter des vivres.</p>

	<p><sup class="versenum">16&nbsp;</sup>J&eacute;sus leur r&eacute;pondit: Ils n&#39;ont pas besoin de s&#39;en aller; donnez-leur vous-m&ecirc;mes &agrave; manger.</p>

	<p><sup class="versenum">17&nbsp;</sup>Mais ils lui dirent: Nous n&#39;avons ici que cinq pains et deux poissons.</p>

	<p><sup class="versenum">18&nbsp;</sup>Et il dit: Apportez-les-moi.</p>

	<p><sup class="versenum">19&nbsp;</sup>Il fit asseoir la foule sur l&#39;herbe, prit les cinq pains et les deux poissons, et, levant les yeux vers le ciel, il rendit gr&acirc;ces. Puis, il rompit les pains et les donna aux disciples, qui les distribu&egrave;rent &agrave; la foule.</p>

	<p><sup class="versenum">20&nbsp;</sup>Tous mang&egrave;rent et furent rassasi&eacute;s, et l&#39;on emporta douze paniers pleins des morceaux qui restaient.</p>

	<p><sup class="versenum">21&nbsp;</sup>Ceux qui avaient mang&eacute; &eacute;taient environ cinq mille hommes, sans les femmes et les enfants.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop3')"> Marc 6:35-4</span>.

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">35&nbsp;</sup>Comme l&#39;heure &eacute;tait d&eacute;j&agrave; avanc&eacute;e, ses disciples s&#39;approch&egrave;rent de lui, et dirent: Ce lieu est d&eacute;sert, et l&#39;heure est d&eacute;j&agrave; avanc&eacute;e;</p>
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

			<td class="social" @click="share('lesson', 'Leadership et Provision: ', '/content/M2/fra/multiply2/multiply236.html')">
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