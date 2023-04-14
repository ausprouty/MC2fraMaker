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
                        <div class="chapter_number ltr"><h1>38.</h1></div>
                        <div class="chapter_title ltr"><h1>La Moisson d'une vie transformée</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <h2>&nbsp;</h2>

<div class="back">
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
</div>

<div class="up">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Marc 7:31-8:9 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Marc 7:31-8:9</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<div>
<div>
<div>
<div>
<div>
<div>
<p><sup class="versenum">31&nbsp;</sup>J&eacute;sus quitta le territoire de Tyr, et revint par Sidon vers la mer de Galil&eacute;e, en traversant le pays de la D&eacute;capole.</p>

<p><sup class="versenum">32&nbsp;</sup>On lui amena un sourd, qui avait de la difficult&eacute; &agrave; parler, et on le pria de lui imposer les mains.</p>

<p><sup class="versenum">33&nbsp;</sup>Il le prit &agrave; part loin de la foule, lui mit les doigts dans les oreilles, et lui toucha la langue avec sa propre salive;</p>

<p><sup class="versenum">34&nbsp;</sup>puis, levant les yeux au ciel, il soupira, et dit: &Eacute;phphatha, c&#39;est-&agrave;-dire, ouvre-toi.</p>

<p><sup class="versenum">35&nbsp;</sup>Aussit&ocirc;t ses oreilles s&#39;ouvrirent, sa langue se d&eacute;lia, et il parla tr&egrave;s bien.</p>

<p><sup class="versenum">36&nbsp;</sup>J&eacute;sus leur recommanda de n&#39;en parler &agrave; personne; mais plus il le leur recommanda, plus ils le publi&egrave;rent.</p>

<p><sup class="versenum">37&nbsp;</sup>Ils &eacute;taient dans le plus grand &eacute;tonnement, et disaient: Il fait tout &agrave; merveille; m&ecirc;me il fait entendre les sourds, et parler les muets.</p>

<p><sup class="versenum">1 </sup>En ces jours-l&agrave;, une foule nombreuse s&#39;&eacute;tant de nouveau r&eacute;unie et n&#39;ayant pas de quoi manger, J&eacute;sus appela les disciples, et leur dit:</p>

<p><sup class="versenum">2&nbsp;</sup>Je suis &eacute;mu de compassion pour cette foule; car voil&agrave; trois jours qu&#39;ils sont pr&egrave;s de moi, et ils n&#39;ont rien &agrave; manger.</p>

<p><sup class="versenum">3&nbsp;</sup>Si je les renvoie chez eux &agrave; jeun, les forces leur manqueront en chemin; car quelques-uns d&#39;entre eux sont venus de loin.</p>

<p><sup class="versenum">4&nbsp;</sup>Ses disciples lui r&eacute;pondirent: Comment pourrait-on les rassasier de pains, ici, dans un lieu d&eacute;sert?</p>

<p><sup class="versenum">5&nbsp;</sup>J&eacute;sus leur demanda: Combien avez-vous de pains? Sept, r&eacute;pondirent-ils.</p>

<p><sup class="versenum">6&nbsp;</sup>Alors il fit asseoir la foule par terre, prit les sept pains, et, apr&egrave;s avoir rendu gr&acirc;ces, il les rompit, et les donna &agrave; ses disciples pour les distribuer; et ils les distribu&egrave;rent &agrave; la foule.</p>

<p><sup class="versenum">7&nbsp;</sup>Ils avaient encore quelques petits poissons, et J&eacute;sus, ayant rendu gr&acirc;ces, les fit aussi distribuer.</p>

<p><sup class="versenum">8&nbsp;</sup>Ils mang&egrave;rent et furent rassasi&eacute;s, et l&#39;on emporta sept corbeilles pleines des morceaux qui restaient.</p>

<p><sup class="versenum">9&nbsp;</sup>Ils &eacute;taient environ quatre mille. Ensuite J&eacute;sus les renvoya.</p>
</div>
</div>
</div>
</div>
</div>
</div>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/238.mp4" type="button" class="external-movie">
         Regardez &nbsp;Marc 7:31-8:9&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de D&eacute;couverte</h2>

<ul>
	<li>Qu&rsquo;est-ce qui a retenu votre attention ou qu&rsquo;avez-vous aim&eacute; le plus ?</li>
	<li>Qu&rsquo;est ce qui est nouveau ou s&rsquo;est d&eacute;velopp&eacute; &agrave; ce point de l&rsquo;histoire de J&eacute;sus?</li>
	<li>Quelle implication du point de vue de l&rsquo;humanit&eacute; ou de la divinit&eacute; de J&eacute;sus voyez-vous dans ce passage ?</li>
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

<p>&nbsp;J&eacute;sus a donn&eacute; la priorit&eacute; &agrave; la formation et au d&eacute;veloppement de ses futurs leaders du mouvement. Il les emm&egrave;ne en &laquo;retraite&raquo; au nord de Tyr et Sidon, hors de leur pays, loin des pressions du minist&egrave;re. Puis ils traversent et redescendent vers le territoire &eacute;tranger de la D&eacute;capole, sur la rive orientale du lac Galil&eacute;e. C&#39;est la premi&egrave;re visite depuis que l&#39;homme d&eacute;moniaque a &eacute;t&eacute; sauv&eacute; et renvoy&eacute; pour partager son histoire avec sa famille et ses amis. Quel contraste avec la visite pr&eacute;c&eacute;dente quand les gens ont demand&eacute; &agrave; J&eacute;sus de s&#39;en aller! Maintenant que les nouvelles sur lui se r&eacute;pandent, des milliers se rassemblent pour entendre son enseignement et faire l&#39;exp&eacute;rience de son pouvoir dans leurs propres vies. Ils ne vont m&ecirc;me pas &agrave; la maison pour dormir ou manger. Apr&egrave;s 3 jours, J&eacute;sus implique son &eacute;quipe dans une autre exp&eacute;rience d&#39;apprentissage de sa grande compassion pour tous et de Sa capacit&eacute; &agrave; pourvoir. Ils apprennent que le t&eacute;moignage d&#39;une vie transform&eacute;e peut ouvrir la porte &agrave; de nouveaux groupes de personnes. En participant &agrave; l&#39;alimentation miraculeuse de plus de 4000 personnes, ils voient la compassion de J&eacute;sus pour toutes les nations.</p>

<ul>
	<li>Pour une &eacute;tude approfondie <span class="popup-link" @click = "popUp('pop1')"> Matthieu 15:29-38</span>.&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">29&nbsp;</sup>J&eacute;sus quitta ces lieux, et vint pr&egrave;s de la mer de Galil&eacute;e. &Eacute;tant mont&eacute; sur la montagne, il s&#39;y assit.</p>

	<p><sup class="versenum">30&nbsp;</sup>Alors s&#39;approcha de lui une grande foule, ayant avec elle des boiteux, des aveugles, des muets, des estropi&eacute;s, et beaucoup d&#39;autres malades. On les mit &agrave; ses pieds, et il les gu&eacute;rit;</p>

	<p><sup class="versenum">31&nbsp;</sup>en sorte que la foule &eacute;tait dans l&#39;admiration de voir que les muets parlaient, que les estropi&eacute;s &eacute;taient gu&eacute;ris, que les boiteux marchaient, que les aveugles voyaient; et elle glorifiait le Dieu d&#39;Isra&euml;l.</p>

	<p><sup class="versenum">32&nbsp;</sup>J&eacute;sus, ayant appel&eacute; ses disciples, dit: Je suis &eacute;mu de compassion pour cette foule; car voil&agrave; trois jours qu&#39;ils sont pr&egrave;s de moi, et ils n&#39;ont rien &agrave; manger. Je ne veux pas les renvoyer &agrave; jeun, de peur que les forces ne leur manquent en chemin.</p>

	<p><sup class="versenum">33&nbsp;</sup>Les disciples lui dirent: Comment nous procurer dans ce lieu d&eacute;sert assez de pains pour rassasier une si grande foule?</p>

	<p><sup class="versenum">34&nbsp;</sup>J&eacute;sus leur demanda: Combien avez-vous de pains? Sept, r&eacute;pondirent-ils, et quelques petits poissons.</p>

	<p><sup class="versenum">35&nbsp;</sup>Alors il fit asseoir la foule par terre,</p>

	<p><sup class="versenum">36&nbsp;</sup>prit les sept pains et les poissons, et, apr&egrave;s avoir rendu gr&acirc;ces, il les rompit et les donna &agrave; ses disciples, qui les distribu&egrave;rent &agrave; la foule.</p>

	<p><sup class="versenum">37&nbsp;</sup>Tous mang&egrave;rent et furent rassasi&eacute;s, et l&#39;on emporta sept corbeilles pleines des morceaux qui restaient.</p>

	<p><sup class="versenum">38&nbsp;</sup>Ceux qui avaient mang&eacute; &eacute;taient quatre mille hommes, sans les femmes et les enfants.</p>
	<!-- end bible --></div>
	</li>
</ul>

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

			<td class="social" @click="share('lesson', 'La Moisson d\'une vie transformée: ', '/content/M2/fra/multiply2/multiply238.html')">
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