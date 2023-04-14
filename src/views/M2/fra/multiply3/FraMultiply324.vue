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
                        <div class="chapter_number ltr"><h1>24.</h1></div>
                        <div class="chapter_title ltr"><h1>Sortie des leaders pour l'accroissement de la mission</h1></div>
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
	<li>Lisez ou observez Actes 13:1-12 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 13:1-12</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Il y avait dans l&#39;&Eacute;glise d&#39;Antioche des proph&egrave;tes et des docteurs: Barnabas, Sim&eacute;on appel&eacute; Niger, Lucius de Cyr&egrave;ne, Manahen, qui avait &eacute;t&eacute; &eacute;lev&eacute; avec H&eacute;rode le t&eacute;trarque, et Saul.</p>

<p><sup class="versenum">2&nbsp;</sup>Pendant qu&#39;ils servaient le Seigneur dans leur minist&egrave;re et qu&#39;ils je&ucirc;naient, le Saint Esprit dit: Mettez-moi &agrave; part Barnabas et Saul pour l&#39;oeuvre &agrave; laquelle je les ai appel&eacute;s.</p>

<p><sup class="versenum">3&nbsp;</sup>Alors, apr&egrave;s avoir je&ucirc;n&eacute; et pri&eacute;, ils leur impos&egrave;rent les mains, et les laiss&egrave;rent partir.</p>

<p><sup class="versenum">4&nbsp;</sup>Barnabas et Saul, envoy&eacute;s par le Saint Esprit, descendirent &agrave; S&eacute;leucie, et de l&agrave; ils s&#39;embarqu&egrave;rent pour l&#39;&icirc;le de Chypre.</p>

<p><sup class="versenum">5&nbsp;</sup>Arriv&eacute;s &agrave; Salamine, ils annonc&egrave;rent la parole de Dieu dans les synagogues des Juifs. Ils avaient Jean pour aide.</p>

<p><sup class="versenum">6&nbsp;</sup>Ayant ensuite travers&eacute; toute l&#39;&icirc;le jusqu&#39;&agrave; Paphos, ils trouv&egrave;rent un certain magicien, faux proph&egrave;te juif, nomm&eacute; Bar J&eacute;sus,</p>

<p><sup class="versenum">7&nbsp;</sup>qui &eacute;tait avec le proconsul Sergius Paulus, homme intelligent. Ce dernier fit appeler Barnabas et Saul, et manifesta le d&eacute;sir d&#39;entendre la parole de Dieu.</p>

<p><sup class="versenum">8&nbsp;</sup>Mais &Eacute;lymas, le magicien, -car c&#39;est ce que signifie son nom, -leur faisait opposition, cherchant &agrave; d&eacute;tourner de la foi le proconsul.</p>

<p><sup class="versenum">9&nbsp;</sup>Alors Saul, appel&eacute; aussi Paul, rempli du Saint Esprit, fixa les regards sur lui, et dit:</p>

<p><sup class="versenum">10&nbsp;</sup>Homme plein de toute esp&egrave;ce de ruse et de fraude, fils du diable, ennemi de toute justice, ne cesseras-tu point de pervertir les voies droites du Seigneur?</p>

<p><sup class="versenum">11&nbsp;</sup>Maintenant voici, la main du Seigneur est sur toi, tu seras aveugle, et pour un temps tu ne verras pas le soleil. Aussit&ocirc;t l&#39;obscurit&eacute; et les t&eacute;n&egrave;bres tomb&egrave;rent sur lui, et il cherchait, en t&acirc;tonnant, des personnes pour le guider.</p>

<p><sup class="versenum">12&nbsp;</sup>Alors le proconsul, voyant ce qui &eacute;tait arriv&eacute;, crut, &eacute;tant frapp&eacute; de la doctrine du Seigneur.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/324.mp4" type="button" class="external-movie">
         Regardez Actes 13:1-12 </button>
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
	<li class="nobreak-final-final">L&#39;&eacute;quipe de direction de l&#39;&eacute;glise d&#39;Antioche &eacute;tait compos&eacute;e de cinq hommes avec des dons et arri&egrave;re-plans diff&eacute;rents. Sous la direction de L&#39;Esprit, ils ont envoy&eacute; Saul et Barnabas, deux membres de l&#39;&eacute;quipe, pour faire des disciples et cr&eacute;er de nouvelles &eacute;glises sur de nouveaux territoires. Barnabas et Saul ont d&eacute;cid&eacute; d&rsquo;emmener avec eux, le jeune cousin de Barnabas, Jean Marc, comme assistant. Le premier endroit qu&#39;ils ont visit&eacute; &eacute;tait Chypre, chez Barnabas, une &icirc;le au large des c&ocirc;tes de la Syrie. Ce sont &eacute;galement des croyants de Chypre qui ont aid&eacute; &agrave; d&eacute;marrer l&#39;&eacute;glise d&#39;Antioche (<span class="popup-link" @click = "popUp('pop3')"> Actes 11:20</span>).&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">20&nbsp;</sup>Il y eut cependant parmi eux quelques hommes de Chypre et de Cyr&egrave;ne, qui, &eacute;tant venus &agrave; Antioche, s&#39;adress&egrave;rent aussi aux Grecs, et leur annonc&egrave;rent la bonne nouvelle du Seigneur J&eacute;sus.</p>
	<!-- end bible --></div>
	Ces relations ont probablement influenc&eacute; leurs plans. En tant que citoyen romain, Saul s&rsquo;est servi de son nom pa&iuml;en, Paul, lors de ses voyages. Paul et Barnabas ont &eacute;t&eacute; pr&eacute;sent&eacute;s au gouverneur de l&#39;&icirc;le par un magicien juif, ce qui a conduit &agrave; un conflit spirituel majeur. Paul n&#39;a pas r&eacute;pondu avec crainte mais avec l&#39;autorit&eacute; de J&eacute;sus (<span class="popup-link" @click = "popUp('pop4')"> Matthieu 28:18-20</span>)&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">18&nbsp;</sup>J&eacute;sus, s&#39;&eacute;tant approch&eacute;, leur parla ainsi: Tout pouvoir m&#39;a &eacute;t&eacute; donn&eacute; dans le ciel et sur la terre.</p>

	<p><sup class="versenum">19&nbsp;</sup>Allez, faites de toutes les nations des disciples, les baptisant au nom du P&egrave;re, du Fils et du Saint Esprit,</p>

	<p><sup class="versenum">20&nbsp;</sup>et enseignez-leur &agrave; observer tout ce que je vous ai prescrit. Et voici, je suis avec vous tous les jours, jusqu&#39;&agrave; la fin du monde.</p>
	</div>

	&nbsp;pour surmonter l&#39;opposition d&eacute;moniaque. La conversion du gouverneur &eacute;tait un &eacute;v&eacute;nement marquant. C&rsquo;&eacute;tait la premi&egrave;re fois qu&#39;un dirigeant politique romain devenait un disciple du Christ.
	</li>
</ul>


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

			<td class="social" @click="share('lesson', 'Sortie des leaders pour l\'accroissement de la mission: ', '/content/M2/fra/multiply3/multiply324.html')">
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