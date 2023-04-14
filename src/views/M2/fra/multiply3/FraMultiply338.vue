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
                        <div class="chapter_number ltr"><h1>38.</h1></div>
                        <div class="chapter_title ltr"><h1>Implantation d'église dans la capital d'Asie (Éphèse)</h1></div>
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
	<li>Lisez ou observez Actes 19: 1-10 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 19:1-10</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Pendant qu&#39;Apollos &eacute;tait &agrave; Corinthe, Paul, apr&egrave;s avoir parcouru les hautes provinces de l&#39;Asie, arriva &agrave; &Eacute;ph&egrave;se. Ayant rencontr&eacute; quelques disciples, il leur dit:</p>

<p><sup class="versenum">2&nbsp;</sup>Avez-vous re&ccedil;u le Saint Esprit, quand vous avez cru? Ils lui r&eacute;pondirent: Nous n&#39;avons pas m&ecirc;me entendu dire qu&#39;il y ait un Saint Esprit.</p>

<p><sup class="versenum">3&nbsp;</sup>Il dit: De quel bapt&ecirc;me avez-vous donc &eacute;t&eacute; baptis&eacute;s? Et ils r&eacute;pondirent: Du bapt&ecirc;me de Jean.</p>

<p><sup class="versenum">4&nbsp;</sup>Alors Paul dit: Jean a baptis&eacute; du bapt&ecirc;me de repentance, disant au peuple de croire en celui qui venait apr&egrave;s lui, c&#39;est-&agrave;-dire, en J&eacute;sus.</p>

<p><sup class="versenum">5&nbsp;</sup>Sur ces paroles, ils furent baptis&eacute;s au nom du Seigneur J&eacute;sus.</p>

<p><sup class="versenum">6&nbsp;</sup>Lorsque Paul leur eut impos&eacute; les mains, le Saint Esprit vint sur eux, et ils parlaient en langues et proph&eacute;tisaient.</p>

<p><sup class="versenum">7&nbsp;</sup>Ils &eacute;taient en tout environ douze hommes.</p>

<p><sup class="versenum">8&nbsp;</sup>Ensuite Paul entra dans la synagogue, o&ugrave; il parla librement. Pendant trois mois, il discourut sur les choses qui concernent le royaume de Dieu, s&#39;effor&ccedil;ant de persuader ceux qui l&#39;&eacute;coutaient.</p>

<p><sup class="versenum">9&nbsp;</sup>Mais, comme quelques-uns restaient endurcis et incr&eacute;dules, d&eacute;criant devant la multitude la voie du Seigneur, il se retira d&#39;eux, s&eacute;para les disciples, et enseigna chaque jour dans l&#39;&eacute;cole d&#39;un nomm&eacute; Tyrannus.</p>

<p><sup class="versenum">10&nbsp;</sup>Cela dura deux ans, de sorte que tous ceux qui habitaient l&#39;Asie, Juifs et Grecs, entendirent la parole du Seigneur.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/338.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 19: 1-10&nbsp; </button>
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
	<li class="nobreak-final-final">Lorsque Paul arriva &nbsp;&agrave; &Eacute;ph&egrave;se, il rencontra 12 hommes qui connaissaient l&rsquo;enseignement de Jean-Baptiste, mais rien au sujet de J&eacute;sus ou sur l&rsquo;envoi de l&rsquo;Esprit-Saint. Apr&egrave;s que Paul les a enseign&eacute;s, ils &eacute;taient volontaires pour &ecirc;tre s&rsquo;identifier &agrave; J&eacute;sus, en faisant baptiser en son nom. Ces nouveaux croyants ont fait l&rsquo;exp&eacute;rience de l&rsquo;Esprit-Saint en recevant le don de la proph&eacute;tie. Bien qu&rsquo;Aquilas et Priscille annoncaient la Bonne Nouvelle &agrave; &Eacute;ph&egrave;se, aucun mouvement n&rsquo;a commenc&eacute; jusqu&rsquo;&agrave; ce que Paul y ait commenc&eacute; l&rsquo;enseignement quotidien. Par cons&eacute;quent, l&rsquo;&eacute;vangile se r&eacute;pand de la capitale r&eacute;gionale &agrave; la province de l&rsquo;Asie toute enti&egrave;re (environs 8 million de personnes) en seulement deux ans. Colosse &eacute;tait une des cit&eacute;s de la province d&rsquo;Asie, qui &eacute;tait atteinte depuis ce temps. Lisez <span class="popup-link" @click = "popUp('pop3')"> Colossiens 1:3-8</span>.&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">3&nbsp;</sup>Nous rendons gr&acirc;ces &agrave; Dieu, le P&egrave;re de notre Seigneur J&eacute;sus Christ, et nous ne cessons de prier pour vous,</p>

	<p><sup class="versenum">4&nbsp;</sup>ayant &eacute;t&eacute; inform&eacute;s de votre foi en J&eacute;sus Christ et de votre charit&eacute; pour tous les saints,</p>

	<p><sup class="versenum">5&nbsp;</sup>&agrave; cause de l&#39;esp&eacute;rance qui vous est r&eacute;serv&eacute;e dans les cieux, et que la parole de la v&eacute;rit&eacute;, la parole de l&#39;&Eacute;vangile vous a pr&eacute;c&eacute;demment fait conna&icirc;tre.</p>

	<p><sup class="versenum">6&nbsp;</sup>Il est au milieu de vous, et dans le monde entier; il porte des fruits, et il va grandissant, comme c&#39;est aussi le cas parmi vous, depuis le jour o&ugrave; vous avez entendu et connu la gr&acirc;ce de Dieu conform&eacute;ment &agrave; la v&eacute;rit&eacute;,</p>

	<p><sup class="versenum">7&nbsp;</sup>d&#39;apr&egrave;s les instructions que vous avez re&ccedil;ues d&#39;&Eacute;paphras, notre bien-aim&eacute; compagnon de service, qui est pour vous un fid&egrave;le ministre de Christ,</p>

	<p><sup class="versenum">8&nbsp;</sup>et qui nous a appris de quelle charit&eacute; l&#39;Esprit vous anime.</p>
	<!-- end bible --></div>
	Le r&ocirc;le strat&eacute;gique de Paul a continu&eacute; &agrave; &eacute;voluer. Il a coach&eacute; les mouvements existants dans quatre autres provinces &agrave; travers des lettres et des ambassadeurs. Son long s&eacute;jour dans la ville d&rsquo;&Eacute;ph&egrave;se lui a permis d&rsquo;avoir son plus grand impact. Les leaders ont &eacute;t&eacute; suscit&eacute;s de la moisson et envoy&eacute;s pour implanter des &eacute;glises.</li>
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

			<td class="social" @click="share('lesson', 'Implantation d\'église dans la capital d\'Asie (Éphèse): ', '/content/M2/fra/multiply3/multiply338.html')">
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