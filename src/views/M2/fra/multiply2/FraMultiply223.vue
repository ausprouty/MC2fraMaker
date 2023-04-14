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
                        <div class="chapter_number ltr"><h1>23.</h1></div>
                        <div class="chapter_title ltr"><h1>Sixième Expédition de la Pêche d’hommes</h1></div>
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
	<li>Lisez ou observez Luc 5:27-39 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 5:27-39</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">27&nbsp;</sup>Apr&egrave;s cela, J&eacute;sus sortit, et il vit un publicain, nomm&eacute; L&eacute;vi, assis au lieu des p&eacute;ages. Il lui dit: Suis-moi.</p>

<p><sup class="versenum">28&nbsp;</sup>Et, laissant tout, il se leva, et le suivit.</p>

<p><sup class="versenum">29&nbsp;</sup>L&eacute;vi lui donna un grand festin dans sa maison, et beaucoup de publicains et d&#39;autres personnes &eacute;taient &agrave; table avec eux.</p>

<p><sup class="versenum">30&nbsp;</sup>Les pharisiens et les scribes murmur&egrave;rent, et dirent &agrave; ses disciples: Pourquoi mangez-vous et buvez-vous avec les publicains et les gens de mauvaise vie?</p>

<p><sup class="versenum">31&nbsp;</sup>J&eacute;sus, prenant la parole, leur dit: Ce ne sont pas ceux qui se portent bien qui ont besoin de m&eacute;decin, mais les malades.</p>

<p><sup class="versenum">32&nbsp;</sup>Je ne suis pas venu appeler &agrave; la repentance des justes, mais des p&eacute;cheurs.</p>

<p><sup class="versenum">33&nbsp;</sup>Ils lui dirent: Les disciples de Jean, comme ceux des pharisiens, je&ucirc;nent fr&eacute;quemment et font des pri&egrave;res, tandis que les tiens mangent et boivent.</p>

<p><sup class="versenum">34&nbsp;</sup>Il leur r&eacute;pondit: Pouvez-vous faire je&ucirc;ner les amis de l&#39;&eacute;poux pendant que l&#39;&eacute;poux est avec eux?</p>

<p><sup class="versenum">35&nbsp;</sup>Les jours viendront o&ugrave; l&#39;&eacute;poux leur sera enlev&eacute;, alors ils je&ucirc;neront en ces jours-l&agrave;.</p>

<p><sup class="versenum">36&nbsp;</sup>Il leur dit aussi une parabole: Personne ne d&eacute;chire d&#39;un habit neuf un morceau pour le mettre &agrave; un vieil habit; car, il d&eacute;chire l&#39;habit neuf, et le morceau qu&#39;il en a pris n&#39;est pas assorti au vieux.</p>

<p><sup class="versenum">37&nbsp;</sup>Et personne ne met du vin nouveau dans de vieilles outres; autrement, le vin nouveau fait rompre les outres, il se r&eacute;pand, et les outres sont perdues;</p>

<p><sup class="versenum">38&nbsp;</sup>mais il faut mettre le vin nouveau dans des outres neuves.</p>

<p><sup class="versenum">39&nbsp;</sup>Et personne, apr&egrave;s avoir bu du vin vieux, ne veut du nouveau, car il dit: Le vieux est bon.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/223.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 5:27-39&nbsp; </button>
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

<p>Matthieu &eacute;tait aussi connu sous le nom de L&eacute;vi, fils d&#39;Alph&eacute;e. Il &eacute;tait puissant, mandat&eacute;, digne de confiance, riche et prot&eacute;g&eacute; par Rome pour collecter des imp&ocirc;ts aupr&egrave;s du peuple d&#39;Isra&euml;l. Mais en tant que collecteur d&#39;imp&ocirc;ts, il &eacute;tait d&eacute;test&eacute; par son propre peuple. Vivant &agrave; Caperna&uuml;m, il avait observ&eacute; J&eacute;sus et avait entendu parler de tout ce qu&#39;il faisait. Peut-&ecirc;tre qu&#39;Il avait d&eacute;j&agrave; l&rsquo;intention de tout abandonner pour suivre J&eacute;sus. Il est clair que le P&egrave;re avait pr&eacute;par&eacute; son c&oelig;ur parce qu&#39;il avait r&eacute;pondu &agrave; l&#39;appel de J&eacute;sus &agrave; le suivre. Imm&eacute;diatement, il a pr&eacute;sent&eacute; J&eacute;sus &agrave; ses amis collecteurs d&#39;imp&ocirc;ts. J&eacute;sus a risqu&eacute; sa r&eacute;putation en tendant la main et en passant du temps &agrave; ce groupe. Mais quel acte d&#39;amour J&eacute;sus a fait preuve en leur accordant la gr&acirc;ce. J&eacute;sus aimait &ecirc;tre connu comme ami des p&eacute;cheurs.</p>

<ul>
	<li class="nobreak-final-final">Etude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Matthieu 9:9-17</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">9&nbsp;</sup>De l&agrave; &eacute;tant all&eacute; plus loin, J&eacute;sus vit un homme assis au lieu des p&eacute;ages, et qui s&#39;appelait Matthieu. Il lui dit: Suis-moi. Cet homme se leva, et le suivit.</p>

	<p><sup class="versenum">10&nbsp;</sup>Comme J&eacute;sus &eacute;tait &agrave; table dans la maison, voici, beaucoup de publicains et de gens de mauvaise vie vinrent se mettre &agrave; table avec lui et avec ses disciples.</p>

	<p><sup class="versenum">11&nbsp;</sup>Les pharisiens virent cela, et ils dirent &agrave; ses disciples: Pourquoi votre ma&icirc;tre mange-t-il avec les publicains et les gens de mauvaise vie?</p>

	<p><sup class="versenum">12&nbsp;</sup>Ce que J&eacute;sus ayant entendu, il dit: Ce ne sont pas ceux qui se portent bien qui ont besoin de m&eacute;decin, mais les malades.</p>

	<p><sup class="versenum">13&nbsp;</sup>Allez, et apprenez ce que signifie: Je prends plaisir &agrave; la mis&eacute;ricorde, et non aux sacrifices. Car je ne suis pas venu appeler des justes, mais des p&eacute;cheurs.</p>

	<p><sup class="versenum">14&nbsp;</sup>Alors les disciples de Jean vinrent aupr&egrave;s de J&eacute;sus, et dirent: Pourquoi nous et les pharisiens je&ucirc;nons-nous, tandis que tes disciples ne je&ucirc;nent point?</p>

	<p><sup class="versenum">15&nbsp;</sup>J&eacute;sus leur r&eacute;pondit: Les amis de l&#39;&eacute;poux peuvent-ils s&#39;affliger pendant que l&#39;&eacute;poux est avec eux? Les jours viendront o&ugrave; l&#39;&eacute;poux leur sera enlev&eacute;, et alors ils je&ucirc;neront.</p>

	<p><sup class="versenum">16&nbsp;</sup>Personne ne met une pi&egrave;ce de drap neuf &agrave; un vieil habit; car elle emporterait une partie de l&#39;habit, et la d&eacute;chirure serait pire.</p>

	<p><sup class="versenum">17&nbsp;</sup>On ne met pas non plus du vin nouveau dans de vieilles outres; autrement, les outres se rompent, le vin se r&eacute;pand, et les outres sont perdues; mais on met le vin nouveau dans des outres neuves, et le vin et les outres se conservent.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> Marc 2:14-22</span>.&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">14&nbsp;</sup>En passant, il vit L&eacute;vi, fils d&#39;Alph&eacute;e, assis au bureau des p&eacute;ages. Il lui dit: Suis-moi. L&eacute;vi se leva, et le suivit.</p>

	<p><sup class="versenum">15&nbsp;</sup>Comme J&eacute;sus &eacute;tait &agrave; table dans la maison de L&eacute;vi, beaucoup de publicains et de gens de mauvaise vie se mirent aussi &agrave; table avec lui et avec ses disciples; car ils &eacute;taient nombreux, et l&#39;avaient suivi.</p>

	<p><sup class="versenum">16&nbsp;</sup>Les scribes et les pharisiens, le voyant manger avec les publicains et les gens de mauvaise vie, dirent &agrave; ses disciples: Pourquoi mange-t-il et boit-il avec les publicains et les gens de mauvaise vie?</p>

	<p><sup class="versenum">17&nbsp;</sup>Ce que J&eacute;sus ayant entendu, il leur dit: Ce ne sont pas ceux qui se portent bien qui ont besoin de m&eacute;decin, mais les malades. Je ne suis pas venu appeler des justes, mais des p&eacute;cheurs.</p>

	<p><sup class="versenum">18&nbsp;</sup>Les disciples de Jean et les pharisiens je&ucirc;naient. Ils vinrent dire &agrave; J&eacute;sus: Pourquoi les disciples de Jean et ceux des pharisiens je&ucirc;nent-ils, tandis que tes disciples ne je&ucirc;nent point?</p>

	<p><sup class="versenum">19&nbsp;</sup>J&eacute;sus leur r&eacute;pondit: Les amis de l&#39;&eacute;poux peuvent-ils je&ucirc;ner pendant que l&#39;&eacute;poux est avec eux? Aussi longtemps qu&#39;ils ont avec eux l&#39;&eacute;poux, ils ne peuvent je&ucirc;ner.</p>

	<p><sup class="versenum">20&nbsp;</sup>Les jours viendront o&ugrave; l&#39;&eacute;poux leur sera enlev&eacute;, et alors ils je&ucirc;neront en ce jour-l&agrave;.</p>

	<p><sup class="versenum">21&nbsp;</sup>Personne ne coud une pi&egrave;ce de drap neuf &agrave; un vieil habit; autrement, la pi&egrave;ce de drap neuf emporterait une partie du vieux, et la d&eacute;chirure serait pire.</p>

	<p><sup class="versenum">22&nbsp;</sup>Et personne ne met du vin nouveau dans de vieilles outres; autrement, le vin fait rompre les outres, et le vin et les outres sont perdus; mais il faut mettre le vin nouveau dans des outres neuves.</p>
	</div>
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

			<td class="social" @click="share('lesson', 'Sixième Expédition de la Pêche d’hommes: ', '/content/M2/fra/multiply2/multiply223.html')">
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