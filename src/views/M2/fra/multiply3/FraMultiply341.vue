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
                        <div class="chapter_number ltr"><h1>41.</h1></div>
                        <div class="chapter_title ltr"><h1>Visites de renforcement des églises (Macédoine et Achaïe)</h1></div>
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
	<li>Lisez ou observez Actes 20:1-12\ deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 20:1-12</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Lorsque le tumulte eut cess&eacute;, Paul r&eacute;unit les disciples, et, apr&egrave;s les avoir exhort&eacute;s, prit cong&eacute; d&#39;eux, et partit pour aller en Mac&eacute;doine.</p>

<p><sup class="versenum">2&nbsp;</sup>Il parcourut cette contr&eacute;e, en adressant aux disciples de nombreuses exhortations.</p>

<p><sup class="versenum">3&nbsp;</sup>Puis il se rendit en Gr&egrave;ce, o&ugrave; il s&eacute;journa trois mois. Il &eacute;tait sur le point de s&#39;embarquer pour la Syrie, quand les Juifs lui dress&egrave;rent des emb&ucirc;ches. Alors il se d&eacute;cida &agrave; reprendre la route de la Mac&eacute;doine.</p>

<p><sup class="versenum">4&nbsp;</sup>Il avait pour l&#39;accompagner jusqu&#39;en Asie: Sopater de B&eacute;r&eacute;e, fils de Pyrrhus, Aristarque et Second de Thessalonique, Ga&iuml;us de Derbe, Timoth&eacute;e, ainsi que Tychique et Trophime, originaires d&#39;Asie.</p>

<p><sup class="versenum">5&nbsp;</sup>Ceux-ci prirent les devants, et nous attendirent &agrave; Troas.</p>

<p><sup class="versenum">6&nbsp;</sup>Pour nous, apr&egrave;s les jours des pains sans levain, nous nous embarqu&acirc;mes &agrave; Philippes, et, au bout de cinq jours, nous les rejoign&icirc;mes &agrave; Troas, o&ugrave; nous pass&acirc;mes sept jours.</p>

<p><sup class="versenum">7&nbsp;</sup>Le premier jour de la semaine, nous &eacute;tions r&eacute;unis pour rompre le pain. Paul, qui devait partir le lendemain, s&#39;entretenait avec les disciples, et il prolongea son discours jusqu&#39;&agrave; minuit.</p>

<p><sup class="versenum">8&nbsp;</sup>Il y avait beaucoup de lampes dans la chambre haute o&ugrave; nous &eacute;tions assembl&eacute;s.</p>

<p><sup class="versenum">9&nbsp;</sup>Or, un jeune homme nomm&eacute; Eutychus, qui &eacute;tait assis sur la fen&ecirc;tre, s&#39;endormit profond&eacute;ment pendant le long discours de Paul; entra&icirc;n&eacute; par le sommeil, il tomba du troisi&egrave;me &eacute;tage en bas, et il fut relev&eacute; mort.</p>

<p><sup class="versenum">10&nbsp;</sup>Mais Paul, &eacute;tant descendu, se pencha sur lui et le prit dans ses bras, en disant: Ne vous troublez pas, car son &acirc;me est en lui.</p>

<p><sup class="versenum">11&nbsp;</sup>Quand il fut remont&eacute;, il rompit le pain et mangea, et il parla longtemps encore jusqu&#39;au jour. Apr&egrave;s quoi il partit.</p>

<p><sup class="versenum">12&nbsp;</sup>Le jeune homme fut ramen&eacute; vivant, et ce fut le sujet d&#39;une grande consolation.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/341.mp4" type="button" class="external-movie">
         Regardez Actes 20:1-12 </button>
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

<ul>
	<li class="nobreak-final-final">Comme &agrave; l&rsquo;accoutum&eacute;, Paul a revisit&eacute; les &eacute;glises qu&rsquo;il a implant&eacute;es afin de les encourag&eacute; et de leur donner plus d&rsquo;enseignement. Il va d&rsquo;abord en Mac&eacute;doine dans les villes de Philippes, Thessalonique et B&eacute;r&eacute;e. Pendant son s&eacute;jour, il &eacute;crivit une autre lettre aux Corinthiens. Apr&egrave;s plusieurs mois a Mac&eacute;doine, Paul s&rsquo;embarqua &agrave; Acha&iuml;e pour visiter les croyants &agrave; Corinthe. Avant son d&eacute;part pour J&eacute;rusalem, il a &eacute;crit une lettre aux &eacute;glises &agrave; Rome pour leur faire connaitre ses plans de voyage et leur expliquer plus en profondeur l&rsquo;&eacute;vangile (<span class="popup-link" @click = "popUp('pop3')"> Romains 1 :11</span>,&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">11&nbsp;</sup>Car je d&eacute;sire vous voir, pour vous communiquer quelque don spirituel, afin que vous soyez affermis,</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop4')"> Romains 15 :28</span>).&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">28&nbsp;</sup>D&egrave;s que j&#39;aurai termin&eacute; cette affaire et que je leur aurai remis ces dons, je partirai pour l&#39;Espagne et passerai chez vous.</p>
	<!-- end bible --></div>
	On voit comment Paul r&eacute;pandait toujours son &eacute;quipe de minist&egrave;re, en d&eacute;veloppant les leaders issus de la moisson pour aller dans le champ de la moisson. Il est mention de sept personnes venues d&rsquo;autres centres de mouvement. On apprend des lettres de Paul, qu&rsquo;il a cr&eacute;&eacute; une unit&eacute; au sein des diff&eacute;rentes &eacute;glises en collectant une offrande pour aider les croyants pauvres &agrave; J&eacute;rusalem. (<span class="popup-link" @click = "popUp('pop5')"> 2 Corinthiens 8 :1-7</span>,&nbsp;

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Nous vous faisons conna&icirc;tre, fr&egrave;res, la gr&acirc;ce de Dieu qui s&#39;est manifest&eacute;e dans les &Eacute;glises de la Mac&eacute;doine.</p>

	<p><sup class="versenum">2&nbsp;</sup>Au milieu de beaucoup de tribulations qui les ont &eacute;prouv&eacute;es, leur joie d&eacute;bordante et leur pauvret&eacute; profonde ont produit avec abondance de riches lib&eacute;ralit&eacute;s de leur part.</p>

	<p><sup class="versenum">3&nbsp;</sup>Ils ont, je l&#39;atteste, donn&eacute; volontairement selon leurs moyens, et m&ecirc;me au del&agrave; de leurs moyens,</p>

	<p><sup class="versenum">4&nbsp;</sup>nous demandant avec de grandes instances la gr&acirc;ce de prendre part &agrave; l&#39;assistance destin&eacute;e aux saints.</p>

	<p><sup class="versenum">5&nbsp;</sup>Et non seulement ils ont contribu&eacute; comme nous l&#39;esp&eacute;rions, mais ils se sont d&#39;abord donn&eacute;s eux-m&ecirc;mes au Seigneur, puis &agrave; nous, par la volont&eacute; de Dieu.</p>

	<p><sup class="versenum">6&nbsp;</sup>Nous avons donc engag&eacute; Tite &agrave; achever chez vous cette oeuvre de bienfaisance, comme il l&#39;avait commenc&eacute;e.</p>

	<p><sup class="versenum">7&nbsp;</sup>De m&ecirc;me que vous excellez en toutes choses, en foi, en parole, en connaissance, en z&egrave;le &agrave; tous &eacute;gards, et dans votre amour pour nous, faites en sorte d&#39;exceller aussi dans cette oeuvre de bienfaisance.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop6')"> Romains 15 :25-26</span>).&nbsp;

	<div class="popup invisible" id="pop6"><!-- begin bible -->
	<p><sup class="versenum">25&nbsp;</sup>Pr&eacute;sentement je vais &agrave; J&eacute;rusalem, pour le service des saints.</p>

	<p><sup class="versenum">26&nbsp;</sup>Car la Mac&eacute;doine et l&#39;Acha&iuml;e ont bien voulu s&#39;imposer une contribution en faveur des pauvres parmi les saints de J&eacute;rusalem.</p>
	<!-- end bible --></div>
	Elle a r&eacute;uni les leaders et les &eacute;glises ensemble pour les aider &agrave; comprendre qu&rsquo;ils font partie d&rsquo;un grand mouvement (<span class="popup-link" @click = "popUp('pop9')"> 1 Thessaloniciens 2:14</span>;&nbsp;

	<div class="popup invisible" id="pop9"><!-- begin bible -->
	<p><sup class="versenum">14&nbsp;</sup>Car vous, fr&egrave;res, vous &ecirc;tes devenus les imitateurs des &Eacute;glises de Dieu qui sont en J&eacute;sus Christ dans la Jud&eacute;e, parce que vous aussi, vous avez souffert de la part de vos propres compatriotes les m&ecirc;mes maux qu&#39;elles ont soufferts de la part des Juifs.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop8')"> 2 Thessaloniciens 1:4</span>).&nbsp;

	<div class="popup invisible" id="pop8"><!-- begin bible -->
	<p><sup class="versenum">4&nbsp;</sup>Aussi nous glorifions-nous de vous dans les &Eacute;glises de Dieu, &agrave; cause de votre pers&eacute;v&eacute;rance et de votre foi au milieu de toutes vos pers&eacute;cutions et des tribulations que vous avez &agrave; supporter.</p>
	<!-- end bible --></div>
	[L&rsquo;&Eacute;pitre aux Romains peut &ecirc;tre lue ici.]</li>
</ul>

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

			<td class="social" @click="share('lesson', 'Visites de renforcement des églises (Macédoine et Achaïe): ', '/content/M2/fra/multiply3/multiply341.html')">
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