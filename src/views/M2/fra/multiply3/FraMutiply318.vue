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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply3-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>18.</h1></div>
                        <div class="chapter_title ltr"><h1>Pierre rend visite aux croyants en Judée</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="lesson">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p><em>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</em></p>

<ul>
	<li class="nobreak-final-final">(Facultatif) J&eacute;sus-Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re ; qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;. Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus-Christ homme, qui s&rsquo;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. (<span class="popup-link" @click = "popUp('pop1')"> Philippiens 2:11</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">11&nbsp;</sup>et que toute langue confesse que J&eacute;sus Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> 1 Timoth&eacute;e 2:4-6</span>)

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">4&nbsp;</sup>qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;.</p>

	<p><sup class="versenum">5&nbsp;</sup>Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus Christ homme,</p>

	<p><sup class="versenum">6&nbsp;</sup>qui s&#39;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. C&#39;est l&agrave; le t&eacute;moignage rendu en son propre temps,</p>
	<!-- end bible --></div>
	</li>
</ul>

</div>

<h2>Soin</h2>

<p><em>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</em></p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la fid&eacute;lit&eacute;</h2>

<p><em>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</em></p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Motivation et encouragement</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p><em>Trouvez un moyen de projeter une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux:</em></p>

<ul>
	<li class="indent">un passage qui leur rappelle le c&oelig;ur du P&egrave;re et de la vision final.</li>
	<li>r&eacute;fl&eacute;chir sur des changements intervenus dans leur vie depuis qu&rsquo;ils ont commenc&eacute; &agrave; suivre Christ</li>
	<li>leur rappeler ce que Dieu veut faire &agrave; travers eux</li>
</ul>

<p><strong>Partagez la GRANDE vision</strong> <em>&laquo; une &eacute;glise pour chaque village et communaut&eacute;, l&rsquo;&eacute;vangile pour chaque personne &raquo;.</em></p>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><p>+ Contexte</p></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<ul>
	<li>Demandez au groupe de raconter l&rsquo;histoire de la semaine pass&eacute;e.</li>
</ul>

</div>

<h2>Lisez</h2>

<ul>
	<li>Lisez ou observez Actes 9:32-43 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 9:32-43</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">32&nbsp;</sup>Comme Pierre visitait tous les saints, il descendit aussi vers ceux qui demeuraient &agrave; Lydde.</p>

<p><sup class="versenum">33&nbsp;</sup>Il y trouva un homme nomm&eacute; &Eacute;n&eacute;e, couch&eacute; sur un lit depuis huit ans, et paralytique.</p>

<p><sup class="versenum">34&nbsp;</sup>Pierre lui dit: &Eacute;n&eacute;e, J&eacute;sus Christ te gu&eacute;rit; l&egrave;ve-toi, et arrange ton lit. Et aussit&ocirc;t il se leva.</p>

<p><sup class="versenum">35&nbsp;</sup>Tous les habitants de Lydde et du Saron le virent, et ils se convertirent au Seigneur.</p>

<p><sup class="versenum">36&nbsp;</sup>Il y avait &agrave; Jopp&eacute;, parmi les disciples, une femme nomm&eacute;e Tabitha, ce qui signifie Dorcas: elle faisait beaucoup de bonnes oeuvres et d&#39;aum&ocirc;nes.</p>

<p><sup class="versenum">37&nbsp;</sup>Elle tomba malade en ce temps-l&agrave;, et mourut. Apr&egrave;s l&#39;avoir lav&eacute;e, on la d&eacute;posa dans une chambre haute.</p>

<p><sup class="versenum">38&nbsp;</sup>Comme Lydde est pr&egrave;s de Jopp&eacute;, les disciples, ayant appris que Pierre s&#39;y trouvait, envoy&egrave;rent deux hommes vers lui, pour le prier de venir chez eux sans tarder.</p>

<p><sup class="versenum">39&nbsp;</sup>Pierre se leva, et partit avec ces hommes. Lorsqu&#39;il fut arriv&eacute;, on le conduisit dans la chambre haute. Toutes les veuves l&#39;entour&egrave;rent en pleurant, et lui montr&egrave;rent les tuniques et les v&ecirc;tements que faisait Dorcas pendant qu&#39;elle &eacute;tait avec elles.</p>

<p><sup class="versenum">40&nbsp;</sup>Pierre fit sortir tout le monde, se mit &agrave; genoux, et pria; puis, se tournant vers le corps, il dit: Tabitha, l&egrave;ve-toi! Elle ouvrit les yeux, et ayant vu Pierre, elle s&#39;assit.</p>

<p><sup class="versenum">41&nbsp;</sup>Il lui donna la main, et la fit lever. Il appela ensuite les saints et les veuves, et la leur pr&eacute;senta vivante.</p>

<p><sup class="versenum">42&nbsp;</sup>Cela fut connu de tout Jopp&eacute;, et beaucoup crurent au Seigneur.</p>

<p><sup class="versenum">43&nbsp;</sup>Pierre demeura quelque temps &agrave; Jopp&eacute;, chez un corroyeur nomm&eacute; Simon.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/318.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 9:32-43&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de d&eacute;couverte</h2>

<ul>
	<li>Qu&rsquo;est-ce qui a retenu votre attention ou qu&rsquo;avez-vous aim&eacute; le plus ? Pourquoi ?</li>
	<li>&Agrave; ce niveau de l&rsquo;histoire, qu&rsquo;est-ce qui est nouveau ou est d&eacute;velopp&eacute; ?</li>
	<li>Quel mod&egrave;le a &eacute;t&eacute; donn&eacute; quant &agrave; la vie d&eacute;pendante de l&rsquo;Esprit, faire de disciples ou au leadership ?</li>
	<li>Comment pouvons-nous vivre diff&eacute;remment maintenant que nous connaissons cette histoire?</li>
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


<p><em>Des questions suppl&eacute;mentaires dont vous pouvez faire usage:</em></p>

<ul>
	<li>Comment les disciples de J&eacute;sus poursuivent-ils Son &oelig;uvre de faire des disciples et d&rsquo;implantation d&rsquo;&eacute;glises ?</li>
	<li>Comment l&rsquo;&eacute;vangile impacte-t-il les gens et la soci&eacute;t&eacute; ?</li>
	<li>Quels &eacute;taient les barri&egrave;res et les obstacles qui ont &eacute;t&eacute; surmont&eacute;s et comment ont-ils &eacute;t&eacute; surmont&eacute;s ?</li>
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


<h2>Lire, raconter et corriger</h2>

<p>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</p>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<p>Pierre commence son voyage en dehors de J&eacute;rusalem, pour visiter les croyants qui se sont install&eacute;s dans d&rsquo;autres villes. L&rsquo;Esprit l&rsquo;utilise pour effectuer plusieurs miracles et amener beaucoup de personnes &agrave; Christ &agrave; Lydde et Jopp&eacute;. Ce sont les premi&egrave;res &eacute;glises en dehors de J&eacute;rusalem que Pierre a aid&eacute; &agrave; d&eacute;marrer. Conduit par l&rsquo;Esprit &agrave; travers la pri&egrave;re, Pierre ram&egrave;ne Tabita &agrave; la vie de la m&ecirc;me fa&ccedil;on qu&rsquo;il vit J&eacute;sus ramener la fille de Ja&iuml;rus. (<span class="popup-link" @click = "popUp('pop3')"> Marc 5:38-42</span>).</p>

<div class="popup invisible" id="pop3"><!-- begin bible -->
<p><sup class="versenum">38&nbsp;</sup>Ils arriv&egrave;rent &agrave; la maison du chef de la synagogue, o&ugrave; J&eacute;sus vit une foule bruyante et des gens qui pleuraient et poussaient de grands cris.</p>

<p><sup class="versenum">39&nbsp;</sup>Il entra, et leur dit: Pourquoi faites-vous du bruit, et pourquoi pleurez-vous? L&#39;enfant n&#39;est pas morte, mais elle dort.</p>

<p><sup class="versenum">40&nbsp;</sup>Et ils se moquaient de lui. Alors, ayant fait sortir tout le monde, il prit avec lui le p&egrave;re et la m&egrave;re de l&#39;enfant, et ceux qui l&#39;avaient accompagn&eacute;, et il entra l&agrave; o&ugrave; &eacute;tait l&#39;enfant.</p>

<p><sup class="versenum">41&nbsp;</sup>Il la saisit par la main, et lui dit: Talitha koumi, ce qui signifie: Jeune fille, l&egrave;ve-toi, je te le dis.</p>

<p><sup class="versenum">42&nbsp;</sup>Aussit&ocirc;t la jeune fille se leva, et se mit &agrave; marcher; car elle avait douze ans. Et ils furent dans un grand &eacute;tonnement.</p>
<!-- end bible --></div>
&nbsp;Jusqu&rsquo;ici, nous avons vu plusieurs exemples de ce que J&eacute;sus a dit de ce qui se passerait &agrave; la venue de L&rsquo;Esprit &nbsp;&laquo; &hellip;celui qui croit en moi fera aussi les &oelig;uvres que je fais, et il en fera de plus grandes &raquo; &nbsp;(<span class="popup-link" @click = "popUp('pop4')"> Jean 14:12</span>).&nbsp;

<div class="popup invisible" id="pop4"><!-- begin bible -->
<p><sup class="versenum">12&nbsp;</sup>En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je vous le dis, celui qui croit en moi fera aussi les oeuvres que je fais, et il en fera de plus grandes, parce que je m&#39;en vais au P&egrave;re;</p>
<!-- end bible --></div>
Tabita est un exemple d&rsquo;une femme qui &eacute;tait active dans le minist&egrave;re en prenant soin des autres et en aidant &agrave; subvenir aux besoins des veuves de la r&eacute;gion. Pierre fait preuve de maturit&eacute; &nbsp;dans sa compr&eacute;hension &nbsp;de la gr&acirc;ce en &eacute;tant dispos&eacute; pour s&eacute;journer dans la maison d&rsquo;un corroyeur, une profession consid&eacute;r&eacute;e comme impure par les termes culturels religieux Juifs.

<p>&nbsp;</p>

<p>&nbsp;</p>
</div>

<p><em>Pratiquez ici la lib&eacute;ralit&eacute; et la sainte-c&egrave;ne ou dans la section Se pr&eacute;parer pour la mission.</em></p>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary4" class="summary"><h2>+ Se pr&eacute;parer pour la mission</h2></div>
<div class="collapsed" id ="Text4">
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

<h2>Aller en mission</h2>

<ul>
	<li>Identifiez des gens vers qui ou des endroits o&ugrave; vous pouvez prendre l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>&Eacute;crivez des promesses &laquo; Je ferai d&rsquo;ici quand &raquo; et partagez cela avec votre petit groupe.</li>
</ul>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note3Text')"
        id="note3Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<h2>Prier pour la mission</h2>

<p>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples.</p>

<h2>B&eacute;n&eacute;diction (facultatif)</h2>
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

			<td class="social" @click="share('lesson', 'Pierre rend visite aux croyants en Judée: ', '/content/M2/fra/multiply3/mutiply318.html')">
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