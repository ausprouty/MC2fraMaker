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
                        <div class="chapter_number ltr"><h1>14.</h1></div>
                        <div class="chapter_title ltr"><h1>Se rappeler du Sacrifice de Jésus</h1></div>
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
	<li>Lisez <span class="popup-link" @click = "popUp('pop1')"> Matthieu 10:28-30</span>&nbsp;&nbsp;et ex&eacute;cutez des chants.

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">28&nbsp;</sup>Ne craignez pas ceux qui tuent le corps et qui ne peuvent tuer l&#39;&acirc;me; craignez plut&ocirc;t celui qui peut faire p&eacute;rir l&#39;&acirc;me et le corps dans la g&eacute;henne.</p>

	<p><sup class="versenum">29&nbsp;</sup>Ne vend-on pas deux passereaux pour un sou? Cependant, il n&#39;en tombe pas un &agrave; terre sans la volont&eacute; de votre P&egrave;re.</p>

	<p><sup class="versenum">30&nbsp;</sup>Et m&ecirc;me les cheveux de votre t&ecirc;te sont tous compt&eacute;s.</p>
	<!-- end bible --></div>
	</li>
	<li>(facultative) Utilisez une d&eacute;claration de foi au sujet de J&eacute;sus, comme <span class="popup-link" @click = "popUp('pop2')"> Philippiens 2:11</span>:&nbsp;
	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">11&nbsp;</sup>et que toute langue confesse que J&eacute;sus Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop3')"> 1 Timoth&eacute;e 2:4-6</span>

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">4&nbsp;</sup>qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;.</p>

	<p><sup class="versenum">5&nbsp;</sup>Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus Christ homme,</p>

	<p><sup class="versenum">6&nbsp;</sup>qui s&#39;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. C&#39;est l&agrave; le t&eacute;moignage rendu en son propre temps,</p>
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

<p>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

<p>Exemple: Lisez <span class="popup-link" @click = "popUp('pop4')"> H&eacute;breux 10:19-25</span></p>

<div class="popup invisible" id="pop4"><!-- begin bible -->
<p><sup class="versenum">19&nbsp;</sup>Ainsi donc, fr&egrave;res, puisque nous avons, au moyen du sang de J&eacute;sus, une libre entr&eacute;e dans le sanctuaire</p>

<p><sup class="versenum">20&nbsp;</sup>par la route nouvelle et vivante qu&#39;il a inaugur&eacute;e pour nous au travers du voile, c&#39;est-&agrave;-dire, de sa chair,</p>

<p><sup class="versenum">21&nbsp;</sup>et puisque nous avons un souverain sacrificateur &eacute;tabli sur la maison de Dieu,</p>

<p><sup class="versenum">22&nbsp;</sup>approchons-nous avec un coeur sinc&egrave;re, dans la pl&eacute;nitude de la foi, les coeurs purifi&eacute;s d&#39;une mauvaise conscience, et le corps lav&eacute; d&#39;une eau pure.</p>

<p><sup class="versenum">23&nbsp;</sup>Retenons fermement la profession de notre esp&eacute;rance, car celui qui a fait la promesse est fid&egrave;le.</p>

<p><sup class="versenum">24&nbsp;</sup>Veillons les uns sur les autres, pour nous exciter &agrave; la charit&eacute; et aux bonnes oeuvres.</p>

<p><sup class="versenum">25&nbsp;</sup>N&#39;abandonnons pas notre assembl&eacute;e, comme c&#39;est la coutume de quelques-uns; mais exhortons-nous r&eacute;ciproquement, et cela d&#39;autant plus que vous voyez s&#39;approcher le jour.</p>
<!-- end bible --></div>
Le Seigneur ne nous a pas appel&eacute;s &agrave; &ecirc;tre seuls. Il nous a appel&eacute;s &agrave; &ecirc;tre ensemble. Nous rencontrons plusieurs d&eacute;fis et nous avons besoin d&rsquo;encouragement et de responsabilit&eacute; pour ob&eacute;ir au Seigneur. Il est mieux de suivre J&eacute;sus en communaut&eacute;. Nous avons besoin les uns des autres, alors ne cessons pas de nous rencontrer!

<p>&nbsp;</p>

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

<p>Dieu a donn&eacute; aux Juifs une c&eacute;l&eacute;bration sp&eacute;ciale appel&eacute;e la P&acirc;que pour qu&rsquo;ils se rappellent de comment il les a d&eacute;livr&eacute;s de l&rsquo;esclavage en Egypte. La nuit qui pr&eacute;c&egrave;de la mort de J&eacute;sus sur la croix, Il c&eacute;l&eacute;bra la P&acirc;que avec ses disciples et expliqua comment cela se r&eacute;f&eacute;rait &agrave; Lui.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Luc 22:14-20 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 22:14-20</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">14&nbsp;</sup>L&#39;heure &eacute;tant venue, il se mit &agrave; table, et les ap&ocirc;tres avec lui.</p>

<p><sup class="versenum">15&nbsp;</sup>Il leur dit: J&#39;ai d&eacute;sir&eacute; vivement manger cette P&acirc;que avec vous, avant de souffrir;</p>

<p><sup class="versenum">16&nbsp;</sup>car, je vous le dis, je ne la mangerai plus, jusqu&#39;&agrave; ce qu&#39;elle soit accomplie dans le royaume de Dieu.</p>

<p><sup class="versenum">17&nbsp;</sup>Et, ayant pris une coupe et rendu gr&acirc;ces, il dit: Prenez cette coupe, et distribuez-la entre vous;</p>

<p><sup class="versenum">18&nbsp;</sup>car, je vous le dis, je ne boirai plus d&eacute;sormais du fruit de la vigne, jusqu&#39;&agrave; ce que le royaume de Dieu soit venu.</p>

<p><sup class="versenum">19&nbsp;</sup>Ensuite il prit du pain; et, apr&egrave;s avoir rendu gr&acirc;ces, il le rompit, et le leur donna, en disant: Ceci est mon corps, qui est donn&eacute; pour vous; faites ceci en m&eacute;moire de moi.</p>

<p><sup class="versenum">20&nbsp;</sup>Il prit de m&ecirc;me la coupe, apr&egrave;s le souper, et la leur donna, en disant: Cette coupe est la nouvelle alliance en mon sang, qui est r&eacute;pandu pour vous.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/114.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 22:14-20&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de D&eacute;couverte</h2>

<ul>
	<li>Chacun dit ce qui a retenu son attention (ou ce qu&rsquo;il a aim&eacute; le plus) et pourquoi.</li>
	<li>Pourquoi pensez-vous que cette histoire est importante?</li>
	<li>Comment pouvons-nous vivre diff&eacute;remment maintenant que nous connaissons cette histoire (ce passage)?</li>
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
	<li>Relisez l&rsquo;histoire. Amenez quelqu&rsquo;un &agrave; raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<p>J&eacute;sus a montr&eacute; &agrave; ses disciples un moyen de se rappeler de sa mort sacrificielle sur la croix. [Prenez un morceau de pain] Le pain repr&eacute;sente Son corps qui a &eacute;t&eacute; bris&eacute; pour nous. [Montrez leur du vin ou du jus] La boisson repr&eacute;sente Son sang qui a &eacute;t&eacute; vers&eacute; pour nous et a ouvert une nouvelle voie pour s&rsquo;adresser &agrave; Dieu. Il leur a recommand&eacute; de continuer &agrave; le pratiquer.</p>

<ul>
	<li class="nobreak-final-final">Dans <span class="popup-link" @click = "popUp('pop5')"> 1 Corinthiens 11:23-30</span>,

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">23&nbsp;</sup>Car j&#39;ai re&ccedil;u du Seigneur ce que je vous ai enseign&eacute;; c&#39;est que le Seigneur J&eacute;sus, dans la nuit o&ugrave; il fut livr&eacute;, prit du pain,</p>

	<p><sup class="versenum">24&nbsp;</sup>et, apr&egrave;s avoir rendu gr&acirc;ces, le rompit, et dit: Ceci est mon corps, qui est rompu pour vous; faites ceci en m&eacute;moire de moi.</p>

	<p><sup class="versenum">25&nbsp;</sup>De m&ecirc;me, apr&egrave;s avoir soup&eacute;, il prit la coupe, et dit: Cette coupe est la nouvelle alliance en mon sang; faites ceci en m&eacute;moire de moi toutes les fois que vous en boirez.</p>

	<p><sup class="versenum">26&nbsp;</sup>Car toutes les fois que vous mangez ce pain et que vous buvez cette coupe, vous annoncez la mort du Seigneur, jusqu&#39;&agrave; ce qu&#39;il vienne.</p>

	<p><sup class="versenum">27&nbsp;</sup>C&#39;est pourquoi celui qui mangera le pain ou boira la coupe du Seigneur indignement, sera coupable envers le corps et le sang du Seigneur.</p>

	<p><sup class="versenum">28&nbsp;</sup>Que chacun donc s&#39;&eacute;prouve soi-m&ecirc;me, et qu&#39;ainsi il mange du pain et boive de la coupe;</p>

	<p><sup class="versenum">29&nbsp;</sup>car celui qui mange et boit sans discerner le corps du Seigneur, mange et boit un jugement contre lui-m&ecirc;me.</p>

	<p><sup class="versenum">30&nbsp;</sup>C&#39;est pour cela qu&#39;il y a parmi vous beaucoup d&#39;infirmes et de malades, et qu&#39;un grand nombre sont morts.</p>
	<!-- end bible --></div>
	nous voyons cela d&egrave;s que Paul commen&ccedil;ait de nouvelles &eacute;glises, il enseignait &agrave; touts les nouveaux croyants comment ob&eacute;ir aux commandements de J&eacute;sus.</li>
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

<p>Pratiquez le repas du Seigneur. Utilisez les pratiques des leaders d&rsquo;&eacute;glises locales ou utilisez celles sugg&eacute;r&eacute;es ci-dessous</p>

<ul>
	<li>Lisez <span class="popup-link" @click = "popUp('pop6')"> 1 Corinthiens 11:23-30</span>

	<div class="popup invisible" id="pop6"><!-- begin bible -->
	<p><sup class="versenum">23&nbsp;</sup>Car j&#39;ai re&ccedil;u du Seigneur ce que je vous ai enseign&eacute;; c&#39;est que le Seigneur J&eacute;sus, dans la nuit o&ugrave; il fut livr&eacute;, prit du pain,</p>

	<p><sup class="versenum">24&nbsp;</sup>et, apr&egrave;s avoir rendu gr&acirc;ces, le rompit, et dit: Ceci est mon corps, qui est rompu pour vous; faites ceci en m&eacute;moire de moi.</p>

	<p><sup class="versenum">25&nbsp;</sup>De m&ecirc;me, apr&egrave;s avoir soup&eacute;, il prit la coupe, et dit: Cette coupe est la nouvelle alliance en mon sang; faites ceci en m&eacute;moire de moi toutes les fois que vous en boirez.</p>

	<p><sup class="versenum">26&nbsp;</sup>Car toutes les fois que vous mangez ce pain et que vous buvez cette coupe, vous annoncez la mort du Seigneur, jusqu&#39;&agrave; ce qu&#39;il vienne.</p>

	<p><sup class="versenum">27&nbsp;</sup>C&#39;est pourquoi celui qui mangera le pain ou boira la coupe du Seigneur indignement, sera coupable envers le corps et le sang du Seigneur.</p>

	<p><sup class="versenum">28&nbsp;</sup>Que chacun donc s&#39;&eacute;prouve soi-m&ecirc;me, et qu&#39;ainsi il mange du pain et boive de la coupe;</p>

	<p><sup class="versenum">29&nbsp;</sup>car celui qui mange et boit sans discerner le corps du Seigneur, mange et boit un jugement contre lui-m&ecirc;me.</p>

	<p><sup class="versenum">30&nbsp;</sup>C&#39;est pour cela qu&#39;il y a parmi vous beaucoup d&#39;infirmes et de malades, et qu&#39;un grand nombre sont morts.</p>
	<!-- end bible --></div>
	.</li>
	<li>Marquez une pause et donnez-leur le temps de confesser leurs p&eacute;ch&eacute;s et parler au Seigneur.</li>
	<li>Donnez le pain, dites leur que ceci repr&eacute;sente Son corps qui a &eacute;t&eacute; bris&eacute; pour nous. Mangez-le ensemble.</li>
	<li>Donnez la boisson. D&icirc;tes-leur que ceci repr&eacute;sente Son sang qui a &eacute;t&eacute; vers&eacute; pour nous. Buvez ensemble.</li>
	<li>Priez et remerciez le Seigneur pour ce qu&rsquo;Il a fait pour nous.</li>
</ul>

<p>&nbsp;</p>

</div>

<h2>Aller en Mission&nbsp;</h2>

<ul>
	<li>Identifiez 5 personnes de votre Liste de R&eacute;seau envers qui vous prendrez l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>Ecrivez les promesses &laquo; Je le ferai d&rsquo;ici quand&raquo;.et parlez-en &agrave; votre groupe</li>
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

<p>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser pour initier un mouvement de faiseurs de disciples.</p>
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

			<td class="social" @click="share('lesson', 'Se rappeler du Sacrifice de Jésus: ', '/content/M2/fra/multiply1/multiply114.html')">
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