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
                        <div class="chapter_number ltr"><h1>35.</h1></div>
                        <div class="chapter_title ltr"><h1>Implantation d'église dans un centre religieux païen  (Athènes)</h1></div>
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
	<li>Lisez ou observez Actes 17:16-34 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 17:16-34</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">16&nbsp;</sup>Comme Paul les attendait &agrave; Ath&egrave;nes, il sentait au dedans de lui son esprit s&#39;irriter, &agrave; la vue de cette ville pleine d&#39;idoles.</p>

<p><sup class="versenum">17&nbsp;</sup>Il s&#39;entretenait donc dans la synagogue avec les Juifs et les hommes craignant Dieu, et sur la place publique chaque jour avec ceux qu&#39;il rencontrait.</p>

<p><sup class="versenum">18&nbsp;</sup>Quelques philosophes &eacute;picuriens et sto&iuml;ciens se mirent &agrave; parler avec lui. Et les uns disaient: Que veut dire ce discoureur? D&#39;autres, l&#39;entendant annoncer J&eacute;sus et la r&eacute;surrection, disaient: Il semble qu&#39;il annonce des divinit&eacute;s &eacute;trang&egrave;res.</p>

<p><sup class="versenum">19&nbsp;</sup>Alors ils le prirent, et le men&egrave;rent &agrave; l&#39;Ar&eacute;opage, en disant: Pourrions-nous savoir quelle est cette nouvelle doctrine que tu enseignes?</p>

<p><sup class="versenum">20&nbsp;</sup>Car tu nous fais entendre des choses &eacute;tranges. Nous voudrions donc savoir ce que cela peut &ecirc;tre.</p>

<p><sup class="versenum">21&nbsp;</sup>Or, tous les Ath&eacute;niens et les &eacute;trangers demeurant &agrave; Ath&egrave;nes ne passaient leur temps qu&#39;&agrave; dire ou &agrave; &eacute;couter des nouvelles.</p>

<p><sup class="versenum">22&nbsp;</sup>Paul, debout au milieu de l&#39;Ar&eacute;opage, dit: Hommes Ath&eacute;niens, je vous trouve &agrave; tous &eacute;gards extr&ecirc;mement religieux.</p>

<p><sup class="versenum">23&nbsp;</sup>Car, en parcourant votre ville et en consid&eacute;rant les objets de votre d&eacute;votion, j&#39;ai m&ecirc;me d&eacute;couvert un autel avec cette inscription: A un dieu inconnu! Ce que vous r&eacute;v&eacute;rez sans le conna&icirc;tre, c&#39;est ce que je vous annonce.</p>

<p><sup class="versenum">24&nbsp;</sup>Le Dieu qui a fait le monde et tout ce qui s&#39;y trouve, &eacute;tant le Seigneur du ciel et de la terre, n&#39;habite point dans des temples faits de main d&#39;homme;</p>

<p><sup class="versenum">25&nbsp;</sup>il n&#39;est point servi par des mains humaines, comme s&#39;il avait besoin de quoi que ce soit, lui qui donne &agrave; tous la vie, la respiration, et toutes choses.</p>

<p><sup class="versenum">26&nbsp;</sup>Il a fait que tous les hommes, sortis d&#39;un seul sang, habitassent sur toute la surface de la terre, ayant d&eacute;termin&eacute; la dur&eacute;e des temps et les bornes de leur demeure;</p>

<p><sup class="versenum">27&nbsp;</sup>il a voulu qu&#39;ils cherchassent le Seigneur, et qu&#39;ils s&#39;effor&ccedil;assent de le trouver en t&acirc;tonnant, bien qu&#39;il ne soit pas loin de chacun de nous,</p>

<p><sup class="versenum">28&nbsp;</sup>car en lui nous avons la vie, le mouvement, et l&#39;&ecirc;tre. C&#39;est ce qu&#39;ont dit aussi quelques-uns de vos po&egrave;tes: De lui nous sommes la race...</p>

<p><sup class="versenum">29&nbsp;</sup>Ainsi donc, &eacute;tant la race de Dieu, nous ne devons pas croire que la divinit&eacute; soit semblable &agrave; de l&#39;or, &agrave; de l&#39;argent, ou &agrave; de la pierre, sculpt&eacute;s par l&#39;art et l&#39;industrie de l&#39;homme.</p>

<p><sup class="versenum">30&nbsp;</sup>Dieu, sans tenir compte des temps d&#39;ignorance, annonce maintenant &agrave; tous les hommes, en tous lieux, qu&#39;ils aient &agrave; se repentir,</p>

<p><sup class="versenum">31&nbsp;</sup>parce qu&#39;il a fix&eacute; un jour o&ugrave; il jugera le monde selon la justice, par l&#39;homme qu&#39;il a d&eacute;sign&eacute;, ce dont il a donn&eacute; &agrave; tous une preuve certaine en le ressuscitant des morts...</p>

<p><sup class="versenum">32&nbsp;</sup>Lorsqu&#39;ils entendirent parler de r&eacute;surrection des morts, les uns se moqu&egrave;rent, et les autres dirent: Nous t&#39;entendrons l&agrave;-dessus une autre fois.</p>

<p><sup class="versenum">33&nbsp;</sup>Ainsi Paul se retira du milieu d&#39;eux.</p>

<p><sup class="versenum">34&nbsp;</sup>Quelques-uns n&eacute;anmoins s&#39;attach&egrave;rent &agrave; lui et crurent, Denys l&#39;ar&eacute;opagite, une femme nomm&eacute;e Damaris, et d&#39;autres avec eux.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/335.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 17:16-34&nbsp; </button>
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

<p>Paul avait une grande compassion pour la perte des gens et &eacute;tait attrist&eacute; par le nombre de faux dieux que les gens essayaient de plaire. Pendant qu&#39;il attendait l&#39;arriv&eacute;e de Silas et Timoth&eacute;e de Mac&eacute;doine, Paul a continu&eacute; &agrave; &eacute;vang&eacute;liser les diff&eacute;rentes personnes de la ville grecque d&#39;Ath&egrave;nes: la petite communaut&eacute; de juifs dans la synagogue locale, sur la place publique des pa&iuml;ens et diff&eacute;rents types de philosophes instruits (comme les professeurs d&#39;universit&eacute;). Cela a conduit les gens qui &eacute;taient curieux du message &agrave; organiser une r&eacute;union avec les dirigeants de la ville. Nous voyons comment Paul a adapt&eacute; son message au public des dirigeants ath&eacute;niens en partant de leur contexte d&#39;avoir un &laquo;dieu inconnu&raquo; et en citant l&#39;un de leurs po&egrave;tes. Paul nous montre que la fa&ccedil;on dont nous communiquons l&#39;&Eacute;vangile peut &ecirc;tre adapt&eacute;e &agrave; diff&eacute;rentes cultures sans changer le message de l&#39;&Eacute;vangile qui est de se repentir et croire en J&eacute;sus. Contrairement &agrave; d&#39;autres villes, il y a eu tr&egrave;s peu de ripostes &agrave; Ath&egrave;nes.</p>

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

			<td class="social" @click="share('lesson', 'Implantation d\'église dans un centre religieux païen  (Athènes): ', '/content/M2/fra/multiply3/multiply335.html')">
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