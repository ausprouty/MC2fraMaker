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
                        <div class="chapter_number ltr"><h1>13.</h1></div>
                        <div class="chapter_title ltr"><h1>La Moisson est prête</h1></div>
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
	<li>Lisez ou observez Jean 4:1-42 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 4:1-42</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Le Seigneur sut que les pharisiens avaient appris qu&#39;il faisait et baptisait plus de disciples que Jean.</p>

<p><sup class="versenum">2&nbsp;</sup>Toutefois J&eacute;sus ne baptisait pas lui-m&ecirc;me, mais c&#39;&eacute;taient ses disciples.</p>

<p><sup class="versenum">3&nbsp;</sup>Alors il quitta la Jud&eacute;e, et retourna en Galil&eacute;e.</p>

<p><sup class="versenum">4&nbsp;</sup>Comme il fallait qu&#39;il pass&acirc;t par la Samarie,</p>

<p><sup class="versenum">5&nbsp;</sup>il arriva dans une ville de Samarie, nomm&eacute;e Sychar, pr&egrave;s du champ que Jacob avait donn&eacute; &agrave; Joseph, son fils.</p>

<p><sup class="versenum">6&nbsp;</sup>L&agrave; se trouvait le puits de Jacob. J&eacute;sus, fatigu&eacute; du voyage, &eacute;tait assis au bord du puits. C&#39;&eacute;tait environ la sixi&egrave;me heure.</p>

<p><sup class="versenum">7&nbsp;</sup>Une femme de Samarie vint puiser de l&#39;eau. J&eacute;sus lui dit: Donne-moi &agrave; boire.</p>

<p><sup class="versenum">8&nbsp;</sup>Car ses disciples &eacute;taient all&eacute;s &agrave; la ville pour acheter des vivres.</p>

<p><sup class="versenum">9&nbsp;</sup>La femme samaritaine lui dit: Comment toi, qui es Juif, me demandes-tu &agrave; boire, &agrave; moi qui suis une femme samaritaine? -Les Juifs, en effet, n&#39;ont pas de relations avec les Samaritains. -</p>

<p><sup class="versenum">10&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Si tu connaissais le don de Dieu et qui est celui qui te dit: Donne-moi &agrave; boire! tu lui aurais toi-m&ecirc;me demand&eacute; &agrave; boire, et il t&#39;aurait donn&eacute; de l&#39;eau vive.</p>

<p><sup class="versenum">11&nbsp;</sup>Seigneur, lui dit la femme, tu n&#39;as rien pour puiser, et le puits est profond; d&#39;o&ugrave; aurais-tu donc cette eau vive?</p>

<p><sup class="versenum">12&nbsp;</sup>Es-tu plus grand que notre p&egrave;re Jacob, qui nous a donn&eacute; ce puits, et qui en a bu lui-m&ecirc;me, ainsi que ses fils et ses troupeaux?</p>

<p><sup class="versenum">13&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Quiconque boit de cette eau aura encore soif;</p>

<p><sup class="versenum">14&nbsp;</sup>mais celui qui boira de l&#39;eau que je lui donnerai n&#39;aura jamais soif, et l&#39;eau que je lui donnerai deviendra en lui une source d&#39;eau qui jaillira jusque dans la vie &eacute;ternelle.</p>

<p><sup class="versenum">15&nbsp;</sup>La femme lui dit: Seigneur, donne-moi cette eau, afin que je n&#39;aie plus soif, et que je ne vienne plus puiser ici.</p>

<p><sup class="versenum">16&nbsp;</sup>Va, lui dit J&eacute;sus, appelle ton mari, et viens ici.</p>

<p><sup class="versenum">17&nbsp;</sup>La femme r&eacute;pondit: Je n&#39;ai point de mari. J&eacute;sus lui dit: Tu as eu raison de dire: Je n&#39;ai point de mari.</p>

<p><sup class="versenum">18&nbsp;</sup>Car tu as eu cinq maris, et celui que tu as maintenant n&#39;est pas ton mari. En cela tu as dit vrai.</p>

<p><sup class="versenum">19&nbsp;</sup>Seigneur, lui dit la femme, je vois que tu es proph&egrave;te.</p>

<p><sup class="versenum">20&nbsp;</sup>Nos p&egrave;res ont ador&eacute; sur cette montagne; et vous dites, vous, que le lieu o&ugrave; il faut adorer est &agrave; J&eacute;rusalem.</p>

<p><sup class="versenum">21&nbsp;</sup>Femme, lui dit J&eacute;sus, crois-moi, l&#39;heure vient o&ugrave; ce ne sera ni sur cette montagne ni &agrave; J&eacute;rusalem que vous adorerez le P&egrave;re.</p>

<p><sup class="versenum">22&nbsp;</sup>Vous adorez ce que vous ne connaissez pas; nous, nous adorons ce que nous connaissons, car le salut vient des Juifs.</p>

<p><sup class="versenum">23&nbsp;</sup>Mais l&#39;heure vient, et elle est d&eacute;j&agrave; venue, o&ugrave; les vrais adorateurs adoreront le P&egrave;re en esprit et en v&eacute;rit&eacute;; car ce sont l&agrave; les adorateurs que le P&egrave;re demande.</p>

<p><sup class="versenum">24&nbsp;</sup>Dieu est Esprit, et il faut que ceux qui l&#39;adorent l&#39;adorent en esprit et en v&eacute;rit&eacute;.</p>

<p><sup class="versenum">25&nbsp;</sup>La femme lui dit: Je sais que le Messie doit venir (celui qu&#39;on appelle Christ); quand il sera venu, il nous annoncera toutes choses.</p>

<p><sup class="versenum">26&nbsp;</sup>J&eacute;sus lui dit: Je le suis, moi qui te parle.</p>

<p><sup class="versenum">27&nbsp;</sup>L&agrave;-dessus arriv&egrave;rent ses disciples, qui furent &eacute;tonn&eacute;s de ce qu&#39;il parlait avec une femme. Toutefois aucun ne dit: Que demandes-tu? ou: De quoi parles-tu avec elle?</p>

<p><sup class="versenum">28&nbsp;</sup>Alors la femme, ayant laiss&eacute; sa cruche, s&#39;en alla dans la ville, et dit aux gens:</p>

<p><sup class="versenum">29&nbsp;</sup>Venez voir un homme qui m&#39;a dit tout ce que j&#39;ai fait; ne serait-ce point le Christ?</p>

<p><sup class="versenum">30&nbsp;</sup>Ils sortirent de la ville, et ils vinrent vers lui.</p>

<p><sup class="versenum">31&nbsp;</sup>Pendant ce temps, les disciples le pressaient de manger, disant: Rabbi, mange.</p>

<p><sup class="versenum">32&nbsp;</sup>Mais il leur dit: J&#39;ai &agrave; manger une nourriture que vous ne connaissez pas.</p>

<p><sup class="versenum">33&nbsp;</sup>Les disciples se disaient donc les uns aux autres: Quelqu&#39;un lui aurait-il apport&eacute; &agrave; manger?</p>

<p><sup class="versenum">34&nbsp;</sup>J&eacute;sus leur dit: Ma nourriture est de faire la volont&eacute; de celui qui m&#39;a envoy&eacute;, et d&#39;accomplir son oeuvre.</p>

<p><sup class="versenum">35&nbsp;</sup>Ne dites-vous pas qu&#39;il y a encore quatre mois jusqu&#39;&agrave; la moisson? Voici, je vous le dis, levez les yeux, et regardez les champs qui d&eacute;j&agrave; blanchissent pour la moisson.</p>

<p><sup class="versenum">36&nbsp;</sup>Celui qui moissonne re&ccedil;oit un salaire, et amasse des fruits pour la vie &eacute;ternelle, afin que celui qui s&egrave;me et celui qui moissonne se r&eacute;jouissent ensemble.</p>

<p><sup class="versenum">37&nbsp;</sup>Car en ceci ce qu&#39;on dit est vrai: Autre est celui qui s&egrave;me, et autre celui qui moissonne.</p>

<p><sup class="versenum">38&nbsp;</sup>Je vous ai envoy&eacute;s moissonner ce que vous n&#39;avez pas travaill&eacute;; d&#39;autres ont travaill&eacute;, et vous &ecirc;tes entr&eacute;s dans leur travail.</p>

<p><sup class="versenum">39&nbsp;</sup>Plusieurs Samaritains de cette ville crurent en J&eacute;sus &agrave; cause de cette d&eacute;claration formelle de la femme: Il m&#39;a dit tout ce que j&#39;ai fait.</p>

<p><sup class="versenum">40&nbsp;</sup>Aussi, quand les Samaritains vinrent le trouver, ils le pri&egrave;rent de rester aupr&egrave;s d&#39;eux. Et il resta l&agrave; deux jours.</p>

<p><sup class="versenum">41&nbsp;</sup>Un beaucoup plus grand nombre crurent &agrave; cause de sa parole;</p>

<p><sup class="versenum">42&nbsp;</sup>et ils disaient &agrave; la femme: Ce n&#39;est plus &agrave; cause de ce que tu as dit que nous croyons; car nous l&#39;avons entendu nous-m&ecirc;mes, et nous savons qu&#39;il est vraiment le Sauveur du monde.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/213.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 4:1-42&nbsp; </button>
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

<p>J&eacute;sus a impliqu&eacute; ses disciples d&egrave;s le d&eacute;but en t&eacute;moignant de Lui et en baptisant les gens dans en vue du mouvement qui grandissait. C&#39;&eacute;tait leur premi&egrave;re affectation de minist&egrave;re. Quand J&eacute;sus a appris que son mouvement grandissant avait &eacute;t&eacute; port&eacute; &agrave; l&#39;attention des chefs religieux &agrave; J&eacute;rusalem, il s&#39;est retir&eacute; avec ses disciples en les emmenant &agrave; travers la r&eacute;gion non-juive de Samarie. Les Juifs avaient une haine et des pr&eacute;jug&eacute;s &eacute;normes contre les Samaritains. J&eacute;sus a bris&eacute; deux normes culturelles: il a parl&eacute; &agrave; un Samaritain et &agrave; une femme! La Samaritaine et les disciples ont &eacute;t&eacute; surpris par cela. Par exemple, J&eacute;sus remodelait l&#39;&eacute;tat d&#39;esprit de ses disciples. Ils ne pouvaient pas voir la personne pr&eacute;par&eacute;e par Dieu et la moisson autour d&#39;eux.</p>

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

			<td class="social" @click="share('lesson', 'La Moisson est prête: ', '/content/M2/fra/multiply2/multiply213.html')">
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