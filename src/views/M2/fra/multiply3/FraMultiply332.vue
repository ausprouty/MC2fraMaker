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
                        <div class="chapter_number ltr"><h1>32.</h1></div>
                        <div class="chapter_title ltr"><h1>Conduit à Macédoine par Jésus (Europe Orientale)</h1></div>
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
	<li>Lisez ou observez Actes 16:6-15 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 16:6-15</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">6&nbsp;</sup>Ayant &eacute;t&eacute; emp&ecirc;ch&eacute;s par le Saint Esprit d&#39;annoncer la parole dans l&#39;Asie, ils travers&egrave;rent la Phrygie et le pays de Galatie.</p>

<p><sup class="versenum">7&nbsp;</sup>Arriv&eacute;s pr&egrave;s de la Mysie, ils se disposaient &agrave; entrer en Bithynie; mais l&#39;Esprit de J&eacute;sus ne le leur permit pas.</p>

<p><sup class="versenum">8&nbsp;</sup>Ils franchirent alors la Mysie, et descendirent &agrave; Troas.</p>

<p><sup class="versenum">9&nbsp;</sup>Pendant la nuit, Paul eut une vision: un Mac&eacute;donien lui apparut, et lui fit cette pri&egrave;re: Passe en Mac&eacute;doine, secours-nous!</p>

<p><sup class="versenum">10&nbsp;</sup>Apr&egrave;s cette vision de Paul, nous cherch&acirc;mes aussit&ocirc;t &agrave; nous rendre en Mac&eacute;doine, concluant que le Seigneur nous appelait &agrave; y annoncer la bonne nouvelle.</p>

<p><sup class="versenum">11&nbsp;</sup>&Eacute;tant partis de Troas, nous f&icirc;mes voile directement vers la Samothrace, et le lendemain nous d&eacute;barqu&acirc;mes &agrave; N&eacute;apolis.</p>

<p><sup class="versenum">12&nbsp;</sup>De l&agrave; nous all&acirc;mes &agrave; Philippes, qui est la premi&egrave;re ville d&#39;un district de Mac&eacute;doine, et une colonie. Nous pass&acirc;mes quelques jours dans cette ville.</p>

<p><sup class="versenum">13&nbsp;</sup>Le jour du sabbat, nous nous rend&icirc;mes, hors de la porte, vers une rivi&egrave;re, o&ugrave; nous pensions que se trouvait un lieu de pri&egrave;re. Nous nous ass&icirc;mes, et nous parl&acirc;mes aux femmes qui &eacute;taient r&eacute;unies.</p>

<p><sup class="versenum">14&nbsp;</sup>L&#39;une d&#39;elles, nomm&eacute;e Lydie, marchande de pourpre, de la ville de Thyatire, &eacute;tait une femme craignant Dieu, et elle &eacute;coutait. Le Seigneur lui ouvrit le coeur, pour qu&#39;elle f&ucirc;t attentive &agrave; ce que disait Paul.</p>

<p><sup class="versenum">15&nbsp;</sup>Lorsqu&#39;elle eut &eacute;t&eacute; baptis&eacute;e, avec sa famille, elle nous fit cette demande: Si vous me jugez fid&egrave;le au Seigneur, entrez dans ma maison, et demeurez-y. Et elle nous pressa par ses instances.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/332.mp4" type="button" class="external-movie">
         Regardez Actes 16:6-15 </button>
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
	<li class="nobreak-final-final">Paul planifiait d&rsquo;aller dans la province d&#39;Asie, qui est &agrave; l&#39;ouest de la Galatie ; mais le Seigneur avait d&#39;autres plans pour l&#39;&eacute;quipe du minist&egrave;re. Ayant &eacute;t&eacute; emp&ecirc;ch&eacute;e par le Saint-Esprit d&#39;aller &agrave; l&#39;ouest en Asie et au nord-est en Bithynie, l&#39;&eacute;quipe s&#39;est rendue au nord-ouest de la ville de Troas sur la c&ocirc;te ouest de la Turquie moderne. Luc, l&#39;auteur du livre des Actes, a rejoint l&#39;&eacute;quipe &agrave; Troas comme l&rsquo;indique l&#39;utilisation de &laquo;nous&raquo; (<span class="popup-link" @click = "popUp('pop3')"> Actes 16:10</span>).&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">10&nbsp;</sup>Apr&egrave;s cette vision de Paul, nous cherch&acirc;mes aussit&ocirc;t &agrave; nous rendre en Mac&eacute;doine, concluant que le Seigneur nous appelait &agrave; y annoncer la bonne nouvelle.</p>
	<!-- end bible --></div>
	Pendant que l&rsquo;&eacute;quipe cherchait la face du Seigneur pour ses prochaines &eacute;tapes, J&eacute;sus a donn&eacute; une vision &agrave; Paul. En &eacute;coutant le Saint-Esprit et en consid&eacute;rant la vision de Paul, ils ont conclu que le Seigneur voulait qu&rsquo;ils se rendent dans la province de Mac&eacute;doine. &Agrave; leur arriv&eacute;e, ils se sont rendus dans la ville strat&eacute;giquement importante de Philippes. Le Seigneur les a conduits vers une personne de paix nomm&eacute;e Lydie, une femme d&#39;affaires de la province d&#39;Asie. Elle a non seulement accueilli le message et l&#39;&eacute;quipe du minist&egrave;re, mais elle a &eacute;galement conduit toute sa famille &agrave; la foi en J&eacute;sus. Comme dans d&#39;autres histoires, le premier acte d&#39;ob&eacute;issance pour ces nouveaux croyants a &eacute;t&eacute; de se faire baptiser.</li>
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

			<td class="social" @click="share('lesson', 'Conduit à Macédoine par Jésus (Europe Orientale): ', '/content/M2/fra/multiply3/multiply332.html')">
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