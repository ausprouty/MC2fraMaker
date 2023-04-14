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
                        <div class="chapter_number ltr"><h1>40.</h1></div>
                        <div class="chapter_title ltr"><h1>Multiplication par la réduction de la cible</h1></div>
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
	<li>Lisez ou observez Luc 9:28-36 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 9:28-36</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">28&nbsp;</sup>Environ huit jours apr&egrave;s qu&#39;il eut dit ces paroles, J&eacute;sus prit avec lui Pierre, Jean et Jacques, et il monta sur la montagne pour prier.</p>

<p><sup class="versenum">29&nbsp;</sup>Pendant qu&#39;il priait, l&#39;aspect de son visage changea, et son v&ecirc;tement devint d&#39;une &eacute;clatante blancheur.</p>

<p><sup class="versenum">30&nbsp;</sup>Et voici, deux hommes s&#39;entretenaient avec lui: c&#39;&eacute;taient Mo&iuml;se et &Eacute;lie,</p>

<p><sup class="versenum">31&nbsp;</sup>qui, apparaissant dans la gloire, parlaient de son d&eacute;part qu&#39;il allait accomplir &agrave; J&eacute;rusalem.</p>

<p><sup class="versenum">32&nbsp;</sup>Pierre et ses compagnons &eacute;taient appesantis par le sommeil; mais, s&#39;&eacute;tant tenus &eacute;veill&eacute;s, ils virent la gloire de J&eacute;sus et les deux hommes qui &eacute;taient avec lui.</p>

<p><sup class="versenum">33&nbsp;</sup>Au moment o&ugrave; ces hommes se s&eacute;paraient de J&eacute;sus, Pierre lui dit: Ma&icirc;tre, il est bon que nous soyons ici; dressons trois tentes, une pour toi, une pour Mo&iuml;se, et une pour &Eacute;lie. Il ne savait ce qu&#39;il disait.</p>

<p><sup class="versenum">34&nbsp;</sup>Comme il parlait ainsi, une nu&eacute;e vint les couvrir; et les disciples furent saisis de frayeur en les voyant entrer dans la nu&eacute;e.</p>

<p><sup class="versenum">35&nbsp;</sup>Et de la nu&eacute;e sortit une voix, qui dit: Celui-ci est mon Fils &eacute;lu: &eacute;coutez-le!</p>

<p><sup class="versenum">36&nbsp;</sup>Quand la voix se fit entendre, J&eacute;sus se trouva seul. Les disciples gard&egrave;rent le silence, et ils ne racont&egrave;rent &agrave; personne, en ce temps-l&agrave;, rien de ce qu&#39;ils avaient vu.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/240.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 9:28-36&nbsp; </button>
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

<p>Six jours apr&egrave;s la confession de Pierre au sujet de qui J&eacute;sus est, J&eacute;sus commence par enseigner au sujet de la souffrance comme faisant partie de l&rsquo;expansion du Royaume. J&eacute;sus choisit trois d&rsquo;entre les 12 leaders et les mets &agrave; part. Pierre, Jacques et Jean se rapprochent encore plus de Lui afin qu&#39;Il puisse leur r&eacute;v&eacute;ler plus au sujet de qui Il est et leur donner une instruction sp&eacute;ciale en tant que leaders des leaders. Il laisse les 9 et prend les 3 au sommet d&#39;une montagne et leur permet de voir Sa pleine gloire r&eacute;v&eacute;l&eacute;e. C&#39;est l&agrave; qu&#39;ils entendent la voix du P&egrave;re, affirmant que J&eacute;sus est Son Fils. M&ecirc;me si Mo&iuml;se et &Eacute;lie &eacute;taient des h&eacute;ros pour le peuple juif, le P&egrave;re met J&eacute;sus au-dessus de tous les autres et dit aux 3 de &laquo; l&#39;&eacute;couter &raquo;.</p>

<p>&nbsp;</p>

<ul>
	<li class="nobreak-final-final">Pour une &eacute;tude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Matthieu 17:1-13</span>;

<div class="popup invisible" id="pop1"><!-- begin bible -->
<p><sup class="versenum">1 </sup>Six jours apr&egrave;s, J&eacute;sus prit avec lui Pierre, Jacques, et Jean, son fr&egrave;re, et il les conduisit &agrave; l&#39;&eacute;cart sur une haute montagne.</p>

<p><sup class="versenum">2&nbsp;</sup>Il fut transfigur&eacute; devant eux; son visage resplendit comme le soleil, et ses v&ecirc;tements devinrent blancs comme la lumi&egrave;re.</p>

<p><sup class="versenum">3&nbsp;</sup>Et voici, Mo&iuml;se et &Eacute;lie leur apparurent, s&#39;entretenant avec lui.</p>

<p><sup class="versenum">4&nbsp;</sup>Pierre, prenant la parole, dit &agrave; J&eacute;sus: Seigneur, il est bon que nous soyons ici; si tu le veux, je dresserai ici trois tentes, une pour toi, une pour Mo&iuml;se, et une pour &Eacute;lie.</p>

<p><sup class="versenum">5&nbsp;</sup>Comme il parlait encore, une nu&eacute;e lumineuse les couvrit. Et voici, une voix fit entendre de la nu&eacute;e ces paroles: Celui-ci est mon Fils bien-aim&eacute;, en qui j&#39;ai mis toute mon affection: &eacute;coutez-le!</p>

<p><sup class="versenum">6&nbsp;</sup>Lorsqu&#39;ils entendirent cette voix, les disciples tomb&egrave;rent sur leur face, et furent saisis d&#39;une grande frayeur.</p>

<p><sup class="versenum">7&nbsp;</sup>Mais J&eacute;sus, s&#39;approchant, les toucha, et dit: Levez-vous, n&#39;ayez pas peur!</p>

<p><sup class="versenum">8&nbsp;</sup>Ils lev&egrave;rent les yeux, et ne virent que J&eacute;sus seul.</p>

<p><sup class="versenum">9&nbsp;</sup>Comme ils descendaient de la montagne, J&eacute;sus leur donna cet ordre: Ne parlez &agrave; personne de cette vision, jusqu&#39;&agrave; ce que le Fils de l&#39;homme soit ressuscit&eacute; des morts.</p>

<p><sup class="versenum">10&nbsp;</sup>Les disciples lui firent cette question: Pourquoi donc les scribes disent-ils qu&#39;&Eacute;lie doit venir premi&egrave;rement?</p>

<p><sup class="versenum">11&nbsp;</sup>Il r&eacute;pondit: Il est vrai qu&#39;&Eacute;lie doit venir, et r&eacute;tablir toutes choses.</p>

<p><sup class="versenum">12&nbsp;</sup>Mais je vous dis qu&#39;&Eacute;lie est d&eacute;j&agrave; venu, qu&#39;ils ne l&#39;ont pas reconnu, et qu&#39;ils l&#39;ont trait&eacute; comme ils ont voulu. De m&ecirc;me le Fils de l&#39;homme souffrira de leur part.</p>

<p><sup class="versenum">13&nbsp;</sup>Les disciples comprirent alors qu&#39;il leur parlait de Jean Baptiste.</p>
<!-- end bible --></div>
&nbsp;<span class="popup-link" @click = "popUp('pop2')"> Marc 9:2-13</span>.

<div class="popup invisible" id="pop2"><!-- begin bible -->
<p><sup class="versenum">2&nbsp;</sup>Six jours apr&egrave;s, J&eacute;sus prit avec lui Pierre, Jacques et Jean, et il les conduisit seuls &agrave; l&#39;&eacute;cart sur une haute montagne. Il fut transfigur&eacute; devant eux;</p>

<p><sup class="versenum">3&nbsp;</sup>ses v&ecirc;tements devinrent resplendissants, et d&#39;une telle blancheur qu&#39;il n&#39;est pas de foulon sur la terre qui puisse blanchir ainsi.</p>

<p><sup class="versenum">4&nbsp;</sup>&Eacute;lie et Mo&iuml;se leur apparurent, s&#39;entretenant avec J&eacute;sus.</p>

<p><sup class="versenum">5&nbsp;</sup>Pierre, prenant la parole, dit &agrave; J&eacute;sus: Rabbi, il est bon que nous soyons ici; dressons trois tentes, une pour toi, une pour Mo&iuml;se, et une pour &Eacute;lie.</p>

<p><sup class="versenum">6&nbsp;</sup>Car il ne savait que dire, l&#39;effroi les ayant saisis.</p>

<p><sup class="versenum">7&nbsp;</sup>Une nu&eacute;e vint les couvrir, et de la nu&eacute;e sortit une voix: Celui-ci est mon Fils bien-aim&eacute;: &eacute;coutez-le!</p>

<p><sup class="versenum">8&nbsp;</sup>Aussit&ocirc;t les disciples regard&egrave;rent tout autour, et ils ne virent que J&eacute;sus seul avec eux.</p>

<p><sup class="versenum">9&nbsp;</sup>Comme ils descendaient de la montagne, J&eacute;sus leur recommanda de ne dire &agrave; personne ce qu&#39;ils avaient vu, jusqu&#39;&agrave; ce que le Fils de l&#39;homme f&ucirc;t ressuscit&eacute; des morts.</p>

<p><sup class="versenum">10&nbsp;</sup>Ils retinrent cette parole, se demandant entre eux ce que c&#39;est que ressusciter des morts.</p>

<p><sup class="versenum">11&nbsp;</sup>Les disciples lui firent cette question: Pourquoi les scribes disent-ils qu&#39;il faut qu&#39;&Eacute;lie vienne premi&egrave;rement?</p>

<p><sup class="versenum">12&nbsp;</sup>Il leur r&eacute;pondit: &Eacute;lie viendra premi&egrave;rement, et r&eacute;tablira toutes choses. Et pourquoi est-il &eacute;crit du Fils de l&#39;homme qu&#39;il doit souffrir beaucoup et &ecirc;tre m&eacute;pris&eacute;?</p>

<p><sup class="versenum">13&nbsp;</sup>Mais je vous dis qu&#39;&Eacute;lie est venu, et qu&#39;ils l&#39;ont trait&eacute; comme ils ont voulu, selon qu&#39;il est &eacute;crit de lui.</p>
<!-- end bible --></div>

</li>
</ul>

</div>

<p class="year">&nbsp;</p>

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

			<td class="social" @click="share('lesson', 'Multiplication par la réduction de la cible: ', '/content/M2/fra/multiply2/multiply240.html')">
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