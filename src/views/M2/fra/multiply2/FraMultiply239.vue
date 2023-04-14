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
                        <div class="chapter_number ltr"><h1>39.</h1></div>
                        <div class="chapter_title ltr"><h1>Retraite du leadership et évaluation</h1></div>
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
	<li>Lisez ou observez Matthieu 16:13-28 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Matthieu 16:13-28</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">13&nbsp;</sup>J&eacute;sus, &eacute;tant arriv&eacute; dans le territoire de C&eacute;sar&eacute;e de Philippe, demanda &agrave; ses disciples: Qui dit-on que je suis, moi, le Fils de l&#39;homme?</p>

<p><sup class="versenum">14&nbsp;</sup>Ils r&eacute;pondirent: Les uns disent que tu es Jean Baptiste; les autres, &Eacute;lie; les autres, J&eacute;r&eacute;mie, ou l&#39;un des proph&egrave;tes.</p>

<p><sup class="versenum">15&nbsp;</sup>Et vous, leur dit-il, qui dites-vous que je suis?</p>

<p><sup class="versenum">16&nbsp;</sup>Simon Pierre r&eacute;pondit: Tu es le Christ, le Fils du Dieu vivant.</p>

<p><sup class="versenum">17&nbsp;</sup>J&eacute;sus, reprenant la parole, lui dit: Tu es heureux, Simon, fils de Jonas; car ce ne sont pas la chair et le sang qui t&#39;ont r&eacute;v&eacute;l&eacute; cela, mais c&#39;est mon P&egrave;re qui est dans les cieux.</p>

<p><sup class="versenum">18&nbsp;</sup>Et moi, je te dis que tu es Pierre, et que sur cette pierre je b&acirc;tirai mon &Eacute;glise, et que les portes du s&eacute;jour des morts ne pr&eacute;vaudront point contre elle.</p>

<p><sup class="versenum">19&nbsp;</sup>Je te donnerai les clefs du royaume des cieux: ce que tu lieras sur la terre sera li&eacute; dans les cieux, et ce que tu d&eacute;lieras sur la terre sera d&eacute;li&eacute; dans les cieux.</p>

<p><sup class="versenum">20&nbsp;</sup>Alors il recommanda aux disciples de ne dire &agrave; personne qu&#39;il &eacute;tait le Christ.</p>

<p><sup class="versenum">21&nbsp;</sup>D&egrave;s lors J&eacute;sus commen&ccedil;a &agrave; faire conna&icirc;tre &agrave; ses disciples qu&#39;il fallait qu&#39;il all&acirc;t &agrave; J&eacute;rusalem, qu&#39;il souffr&icirc;t beaucoup de la part des anciens, des principaux sacrificateurs et des scribes, qu&#39;il f&ucirc;t mis &agrave; mort, et qu&#39;il ressuscit&acirc;t le troisi&egrave;me jour.</p>

<p><sup class="versenum">22&nbsp;</sup>Pierre, l&#39;ayant pris &agrave; part, se mit &agrave; le reprendre, et dit: A Dieu ne plaise, Seigneur! Cela ne t&#39;arrivera pas.</p>

<p><sup class="versenum">23&nbsp;</sup>Mais J&eacute;sus, se retournant, dit &agrave; Pierre: Arri&egrave;re de moi, Satan! tu m&#39;es en scandale; car tes pens&eacute;es ne sont pas les pens&eacute;es de Dieu, mais celles des hommes.</p>

<p><sup class="versenum">24&nbsp;</sup>Alors J&eacute;sus dit &agrave; ses disciples: Si quelqu&#39;un veut venir apr&egrave;s moi, qu&#39;il renonce &agrave; lui-m&ecirc;me, qu&#39;il se charge de sa croix, et qu&#39;il me suive.</p>

<p><sup class="versenum">25&nbsp;</sup>Car celui qui voudra sauver sa vie la perdra, mais celui qui la perdra &agrave; cause de moi la trouvera.</p>

<p><sup class="versenum">26&nbsp;</sup>Et que servirait-il &agrave; un homme de gagner tout le monde, s&#39;il perdait son &acirc;me? ou, que donnerait un homme en &eacute;change de son &acirc;me?</p>

<p><sup class="versenum">27&nbsp;</sup>Car le Fils de l&#39;homme doit venir dans la gloire de son P&egrave;re, avec ses anges; et alors il rendra &agrave; chacun selon ses oeuvres.</p>

<p><sup class="versenum">28&nbsp;</sup>Je vous le dis en v&eacute;rit&eacute;, quelques-uns de ceux qui sont ici ne mourront point, qu&#39;ils n&#39;aient vu le Fils de l&#39;homme venir dans son r&egrave;gne.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/239.mp4" type="button" class="external-movie">
         Regardez Matthieu 16:13-28 </button>
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

<p>J&eacute;sus continue par pr&eacute;parer Son &eacute;quipe de leadership pour la mission. Il les enseigne au sujet de l&rsquo;amour, l&rsquo;humilit&eacute;, la foi et leur compr&eacute;hension de l&rsquo;autorit&eacute;. Il les emm&egrave;ne maintenant au nord dans un autre endroit pa&iuml;en non juif. J&eacute;sus commence par &eacute;valuer le minist&egrave;re en demandant &laquo; Qui dit-on que Je suis &raquo;. La question n&rsquo;est pas au sujet des nombres, il s&#39;agit de la question centrale du mouvement. C&rsquo;est la plus importante question que nous pouvons nous poser et poser &agrave; d&rsquo;autres. Apr&egrave;s pr&egrave;s de trois ann&eacute;es de minist&egrave;re public, en disant aux gens qu&rsquo;Il &eacute;tait le Messie, et op&eacute;rant des prodiges qui montraient qu&rsquo;Il &eacute;tait le Messie, les gens continuaient de penser qu&rsquo;Il &eacute;tait Jean, Elie, J&eacute;r&eacute;mie ou un proph&egrave;te. J&eacute;sus demanda alors aux 12 quelle r&eacute;ponse donneraient-ils &agrave; la question. Pierre r&eacute;pondit au nom du groupe, &laquo; Tue s le Christ, le Fils du Dieu vivant &raquo;. Ils ont bien r&eacute;pondu! Mais J&eacute;sus saisit l&rsquo;occasion pour leur rappeler que cette compr&eacute;hension venait du P&egrave;re. Tout ce que nous comprenons au sujet de J&eacute;sus vient du Dieu le P&egrave;re qui ouvre notre compr&eacute;hension, et non par notre propre intellect. C&rsquo;est aussi pour la premi&egrave;re fois que J&eacute;sus mentionne Son &laquo; Eglise &raquo; en disant qu&rsquo;Il la b&acirc;tira sur cette pierre de la fondation de la v&eacute;rit&eacute; qu&rsquo;Il est. J&eacute;sus r&eacute;v&egrave;le que Son Eglise est un mouvement de mission pour toutes les nations. C&rsquo;&eacute;tait sur ce territoire pa&iuml;en qu&rsquo;Il a choisi d&eacute;clarer premi&egrave;rement Son plan. Combien diff&eacute;rente aurait &eacute;t&eacute; leur compr&eacute;hension s&rsquo;Il avait fait cette d&eacute;claration dans le temple de J&eacute;rusalem !</p>

<ul>
	<li class="nobreak-final-final">Pour une &eacute;tude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Marc 8:27-38</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">27&nbsp;</sup>J&eacute;sus s&#39;en alla, avec ses disciples, dans les villages de C&eacute;sar&eacute;e de Philippe, et il leur posa en chemin cette question: Qui dit-on que je suis?</p>

	<p><sup class="versenum">28&nbsp;</sup>Ils r&eacute;pondirent: Jean Baptiste; les autres, &Eacute;lie, les autres, l&#39;un des proph&egrave;tes.</p>

	<p><sup class="versenum">29&nbsp;</sup>Et vous, leur demanda-t-il, qui dites-vous que je suis? Pierre lui r&eacute;pondit: Tu es le Christ.</p>

	<p><sup class="versenum">30&nbsp;</sup>J&eacute;sus leur recommanda s&eacute;v&egrave;rement de ne dire cela de lui &agrave; personne.</p>

	<p><sup class="versenum">31&nbsp;</sup>Alors il commen&ccedil;a &agrave; leur apprendre qu&#39;il fallait que le Fils de l&#39;homme souffr&icirc;t beaucoup, qu&#39;il f&ucirc;t rejet&eacute; par les anciens, par les principaux sacrificateurs et par les scribes, qu&#39;il f&ucirc;t mis &agrave; mort, et qu&#39;il ressuscit&acirc;t trois jours apr&egrave;s.</p>

	<p><sup class="versenum">32&nbsp;</sup>Il leur disait ces choses ouvertement. Et Pierre, l&#39;ayant pris &agrave; part, se mit &agrave; le reprendre.</p>

	<p><sup class="versenum">33&nbsp;</sup>Mais J&eacute;sus, se retournant et regardant ses disciples, r&eacute;primanda Pierre, et dit: Arri&egrave;re de moi, Satan! car tu ne con&ccedil;ois pas les choses de Dieu, tu n&#39;as que des pens&eacute;es humaines.</p>

	<p><sup class="versenum">34&nbsp;</sup>Puis, ayant appel&eacute; la foule avec ses disciples, il leur dit: Si quelqu&#39;un veut venir apr&egrave;s moi, qu&#39;il renonce &agrave; lui-m&ecirc;me, qu&#39;il se charge de sa croix, et qu&#39;il me suive.</p>

	<p><sup class="versenum">35&nbsp;</sup>Car celui qui voudra sauver sa vie la perdra, mais celui qui perdra sa vie &agrave; cause de moi et de la bonne nouvelle la sauvera.</p>

	<p><sup class="versenum">36&nbsp;</sup>Et que sert-il &agrave; un homme de gagner tout le monde, s&#39;il perd son &acirc;me?</p>

	<p><sup class="versenum">37&nbsp;</sup>Que donnerait un homme en &eacute;change de son &acirc;me?</p>

	<p><sup class="versenum">38&nbsp;</sup>Car quiconque aura honte de moi et de mes paroles au milieu de cette g&eacute;n&eacute;ration adult&egrave;re et p&eacute;cheresse, le Fils de l&#39;homme aura aussi honte de lui, quand il viendra dans la gloire de son P&egrave;re, avec les saints anges.</p>
	<!-- end bible --></div>
	&nbsp;<span class="popup-link" @click = "popUp('pop2')"> Luc 9:18-27</span>.

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">18&nbsp;</sup>Un jour que J&eacute;sus priait &agrave; l&#39;&eacute;cart, ayant avec lui ses disciples, il leur posa cette question: Qui dit-on que je suis?</p>

	<p><sup class="versenum">19&nbsp;</sup>Ils r&eacute;pondirent: Jean Baptiste; les autres, &Eacute;lie; les autres, qu&#39;un des anciens proph&egrave;tes est ressuscit&eacute;.</p>

	<p><sup class="versenum">20&nbsp;</sup>Et vous, leur demanda-t-il, qui dites-vous que je suis? Pierre r&eacute;pondit: Le Christ de Dieu.</p>

	<p><sup class="versenum">21&nbsp;</sup>J&eacute;sus leur recommanda s&eacute;v&egrave;rement de ne le dire &agrave; personne.</p>

	<p><sup class="versenum">22&nbsp;</sup>Il ajouta qu&#39;il fallait que le Fils de l&#39;homme souffr&icirc;t beaucoup, qu&#39;il f&ucirc;t rejet&eacute; par les anciens, par les principaux sacrificateurs et par les scribes, qu&#39;il f&ucirc;t mis &agrave; mort, et qu&#39;il ressuscit&acirc;t le troisi&egrave;me jour.</p>

	<p><sup class="versenum">23&nbsp;</sup>Puis il dit &agrave; tous: Si quelqu&#39;un veut venir apr&egrave;s moi, qu&#39;il renonce &agrave; lui-m&ecirc;me, qu&#39;il se charge chaque jour de sa croix, et qu&#39;il me suive.</p>

	<p><sup class="versenum">24&nbsp;</sup>Car celui qui voudra sauver sa vie la perdra, mais celui qui la perdra &agrave; cause de moi la sauvera.</p>

	<p><sup class="versenum">25&nbsp;</sup>Et que servirait-il &agrave; un homme de gagner tout le monde, s&#39;il se d&eacute;truisait ou se perdait lui-m&ecirc;me?</p>

	<p><sup class="versenum">26&nbsp;</sup>Car quiconque aura honte de moi et de mes paroles, le Fils de l&#39;homme aura honte de lui, quand il viendra dans sa gloire, et dans celle du P&egrave;re et des saints anges.</p>

	<p><sup class="versenum">27&nbsp;</sup>Je vous le dis en v&eacute;rit&eacute;, quelques-uns de ceux qui sont ici ne mourront point qu&#39;ils n&#39;aient vu le royaume de Dieu.</p>
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

			<td class="social" @click="share('lesson', 'Retraite du leadership et évaluation: ', '/content/M2/fra/multiply2/multiply239.html')">
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