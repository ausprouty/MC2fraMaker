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
                        <div class="chapter_number ltr"><h1>41.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership, Grâce et Compassion</h1></div>
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
	<li>Lisez ou observez Jean 7:1-8:11 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 7:1-8:11</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<div>
<div>
<div>
<div>
<div>
<div>
<p><sup class="versenum">1 </sup>Apr&egrave;s cela, J&eacute;sus parcourait la Galil&eacute;e, car il ne voulait pas s&eacute;journer en Jud&eacute;e, parce que les Juifs cherchaient &agrave; le faire mourir.</p>

<p><sup class="versenum">2&nbsp;</sup>Or, la f&ecirc;te des Juifs, la f&ecirc;te des Tabernacles, &eacute;tait proche.</p>

<p><sup class="versenum">3&nbsp;</sup>Et ses fr&egrave;res lui dirent: Pars d&#39;ici, et va en Jud&eacute;e, afin que tes disciples voient aussi les oeuvres que tu fais.</p>

<p><sup class="versenum">4&nbsp;</sup>Personne n&#39;agit en secret, lorsqu&#39;il d&eacute;sire para&icirc;tre: si tu fais ces choses, montre-toi toi-m&ecirc;me au monde.</p>

<p><sup class="versenum">5&nbsp;</sup>Car ses fr&egrave;res non plus ne croyaient pas en lui.</p>

<p><sup class="versenum">6&nbsp;</sup>J&eacute;sus leur dit: Mon temps n&#39;est pas encore venu, mais votre temps est toujours pr&ecirc;t.</p>

<p><sup class="versenum">7&nbsp;</sup>Le monde ne peut vous ha&iuml;r; moi, il me hait, parce que je rends de lui le t&eacute;moignage que ses oeuvres sont mauvaises.</p>

<p><sup class="versenum">8&nbsp;</sup>Montez, vous, &agrave; cette f&ecirc;te; pour moi, je n&#39;y monte point, parce que mon temps n&#39;est pas encore accompli.</p>

<p><sup class="versenum">9&nbsp;</sup>Apr&egrave;s leur avoir dit cela, il resta en Galil&eacute;e.</p>

<p><sup class="versenum">10&nbsp;</sup>Lorsque ses fr&egrave;res furent mont&eacute;s &agrave; la f&ecirc;te, il y monta aussi lui-m&ecirc;me, non publiquement, mais comme en secret.</p>

<p><sup class="versenum">11&nbsp;</sup>Les Juifs le cherchaient pendant la f&ecirc;te, et disaient: O&ugrave; est-il?</p>

<p><sup class="versenum">12&nbsp;</sup>Il y avait dans la foule grande rumeur &agrave; son sujet. Les uns disaient: C&#39;est un homme de bien. D&#39;autres disaient: Non, il &eacute;gare la multitude.</p>

<p><sup class="versenum">13&nbsp;</sup>Personne, toutefois, ne parlait librement de lui, par crainte des Juifs.</p>

<p><sup class="versenum">14&nbsp;</sup>Vers le milieu de la f&ecirc;te, J&eacute;sus monta au temple. Et il enseignait.</p>

<p><sup class="versenum">15&nbsp;</sup>Les Juifs s&#39;&eacute;tonnaient, disant: Comment conna&icirc;t-il les &Eacute;critures, lui qui n&#39;a point &eacute;tudi&eacute;?</p>

<p><sup class="versenum">16&nbsp;</sup>J&eacute;sus leur r&eacute;pondit: Ma doctrine n&#39;est pas de moi, mais de celui qui m&#39;a envoy&eacute;.</p>

<p><sup class="versenum">17&nbsp;</sup>Si quelqu&#39;un veut faire sa volont&eacute;, il conna&icirc;tra si ma doctrine est de Dieu, ou si je parle de mon chef.</p>

<p><sup class="versenum">18&nbsp;</sup>Celui qui parle de son chef cherche sa propre gloire; mais celui qui cherche la gloire de celui qui l&#39;a envoy&eacute;, celui-l&agrave; est vrai, et il n&#39;y a point d&#39;injustice en lui.</p>

<p><sup class="versenum">19&nbsp;</sup>Mo&iuml;se ne vous a-t-il pas donn&eacute; la loi? Et nul de vous n&#39;observe la loi. Pourquoi cherchez-vous &agrave; me faire mourir?</p>

<p><sup class="versenum">20&nbsp;</sup>La foule r&eacute;pondit: Tu as un d&eacute;mon. Qui est-ce qui cherche &agrave; te faire mourir?</p>

<p><sup class="versenum">21&nbsp;</sup>J&eacute;sus leur r&eacute;pondit: J&#39;ai fait une oeuvre, et vous en &ecirc;tes tous &eacute;tonn&eacute;s.</p>

<p><sup class="versenum">22&nbsp;</sup>Mo&iuml;se vous a donn&eacute; la circoncision, -non qu&#39;elle vienne de Mo&iuml;se, car elle vient des patriarches, -et vous circoncisez un homme le jour du sabbat.</p>

<p><sup class="versenum">23&nbsp;</sup>Si un homme re&ccedil;oit la circoncision le jour du sabbat, afin que la loi de Mo&iuml;se ne soit pas viol&eacute;e, pourquoi vous irritez-vous contre moi de ce que j&#39;ai gu&eacute;ri un homme tout entier le jour du sabbat?</p>

<p><sup class="versenum">24&nbsp;</sup>Ne jugez pas selon l&#39;apparence, mais jugez selon la justice.</p>

<p><sup class="versenum">25&nbsp;</sup>Quelques habitants de J&eacute;rusalem disaient: N&#39;est-ce pas l&agrave; celui qu&#39;ils cherchent &agrave; faire mourir?</p>

<p><sup class="versenum">26&nbsp;</sup>Et voici, il parle librement, et ils ne lui disent rien! Est-ce que vraiment les chefs auraient reconnu qu&#39;il est le Christ?</p>

<p><sup class="versenum">27&nbsp;</sup>Cependant celui-ci, nous savons d&#39;o&ugrave; il est; mais le Christ, quand il viendra, personne ne saura d&#39;o&ugrave; il est.</p>

<p><sup class="versenum">28&nbsp;</sup>Et J&eacute;sus, enseignant dans le temple, s&#39;&eacute;cria: Vous me connaissez, et vous savez d&#39;o&ugrave; je suis! Je ne suis pas venu de moi-m&ecirc;me: mais celui qui m&#39;a envoy&eacute; est vrai, et vous ne le connaissez pas.</p>

<p><sup class="versenum">29&nbsp;</sup>Moi, je le connais; car je viens de lui, et c&#39;est lui qui m&#39;a envoy&eacute;.</p>

<p><sup class="versenum">30&nbsp;</sup>Ils cherchaient donc &agrave; se saisir de lui, et personne ne mit la main sur lui, parce que son heure n&#39;&eacute;tait pas encore venue.</p>

<p><sup class="versenum">31&nbsp;</sup>Plusieurs parmi la foule crurent en lui, et ils disaient: Le Christ, quand il viendra, fera-t-il plus de miracles que n&#39;en a fait celui-ci?</p>

<p><sup class="versenum">32&nbsp;</sup>Les pharisiens entendirent la foule murmurant de lui ces choses. Alors les principaux sacrificateurs et les pharisiens envoy&egrave;rent des huissiers pour le saisir.</p>

<p><sup class="versenum">33&nbsp;</sup>J&eacute;sus dit: Je suis encore avec vous pour un peu de temps, puis je m&#39;en vais vers celui qui m&#39;a envoy&eacute;.</p>

<p><sup class="versenum">34&nbsp;</sup>Vous me chercherez et vous ne me trouverez pas, et vous ne pouvez venir o&ugrave; je serai.</p>

<p><sup class="versenum">35&nbsp;</sup>Sur quoi les Juifs dirent entre eux: O&ugrave; ira-t-il, que nous ne le trouvions pas? Ira-t-il parmi ceux qui sont dispers&eacute;s chez les Grecs, et enseignera-t-il les Grecs?</p>

<p><sup class="versenum">36&nbsp;</sup>Que signifie cette parole qu&#39;il a dite: Vous me chercherez et vous ne me trouverez pas, et vous ne pouvez venir o&ugrave; je serai?</p>

<p><sup class="versenum">37&nbsp;</sup>Le dernier jour, le grand jour de la f&ecirc;te, J&eacute;sus, se tenant debout, s&#39;&eacute;cria: Si quelqu&#39;un a soif, qu&#39;il vienne &agrave; moi, et qu&#39;il boive.</p>

<p><sup class="versenum">38&nbsp;</sup>Celui qui croit en moi, des fleuves d&#39;eau vive couleront de son sein, comme dit l&#39;&Eacute;criture.</p>

<p><sup class="versenum">39&nbsp;</sup>Il dit cela de l&#39;Esprit que devaient recevoir ceux qui croiraient en lui; car l&#39;Esprit n&#39;&eacute;tait pas encore, parce que J&eacute;sus n&#39;avait pas encore &eacute;t&eacute; glorifi&eacute;.</p>

<p><sup class="versenum">40&nbsp;</sup>Des gens de la foule, ayant entendu ces paroles, disaient: Celui-ci est vraiment le proph&egrave;te.</p>

<p><sup class="versenum">41&nbsp;</sup>D&#39;autres disaient: C&#39;est le Christ. Et d&#39;autres disaient: Est-ce bien de la Galil&eacute;e que doit venir le Christ?</p>

<p><sup class="versenum">42&nbsp;</sup>L&#39;&Eacute;criture ne dit-elle pas que c&#39;est de la post&eacute;rit&eacute; de David, et du village de Bethl&eacute;hem, o&ugrave; &eacute;tait David, que le Christ doit venir?</p>

<p><sup class="versenum">43&nbsp;</sup>Il y eut donc, &agrave; cause de lui, division parmi la foule.</p>

<p><sup class="versenum">44&nbsp;</sup>Quelques-uns d&#39;entre eux voulaient le saisir, mais personne ne mit la main sur lui.</p>

<p><sup class="versenum">45&nbsp;</sup>Ainsi les huissiers retourn&egrave;rent vers les principaux sacrificateurs et les pharisiens. Et ceux-ci leur dirent: Pourquoi ne l&#39;avez-vous pas amen&eacute;?</p>

<p><sup class="versenum">46&nbsp;</sup>Les huissiers r&eacute;pondirent: Jamais homme n&#39;a parl&eacute; comme cet homme.</p>

<p><sup class="versenum">47&nbsp;</sup>Les pharisiens leur r&eacute;pliqu&egrave;rent: Est-ce que vous aussi, vous avez &eacute;t&eacute; s&eacute;duits?</p>

<p><sup class="versenum">48&nbsp;</sup>Y a-t-il quelqu&#39;un des chefs ou des pharisiens qui ait cru en lui?</p>

<p><sup class="versenum">49&nbsp;</sup>Mais cette foule qui ne conna&icirc;t pas la loi, ce sont des maudits!</p>

<p><sup class="versenum">50&nbsp;</sup>Nicod&egrave;me, qui &eacute;tait venu de nuit vers J&eacute;sus, et qui &eacute;tait l&#39;un d&#39;entre eux, leur dit:</p>

<p><sup class="versenum">51&nbsp;</sup>Notre loi condamne-t-elle un homme avant qu&#39;on l&#39;entende et qu&#39;on sache ce qu&#39;il a fait?</p>

<p><sup class="versenum">52&nbsp;</sup>Ils lui r&eacute;pondirent: Es-tu aussi Galil&eacute;en? Examine, et tu verras que de la Galil&eacute;e il ne sort point de proph&egrave;te.</p>

<p><sup class="versenum">53&nbsp;</sup>Et chacun s&#39;en retourna dans sa maison.</p>

<p><sup class="versenum">1 </sup>J&eacute;sus se rendit &agrave; la montagne des oliviers.</p>

<p><sup class="versenum">2&nbsp;</sup>Mais, d&egrave;s le matin, il alla de nouveau dans le temple, et tout le peuple vint &agrave; lui. S&#39;&eacute;tant assis, il les enseignait.</p>

<p><sup class="versenum">3&nbsp;</sup>Alors les scribes et les pharisiens amen&egrave;rent une femme surprise en adult&egrave;re;</p>

<p><sup class="versenum">4&nbsp;</sup>et, la pla&ccedil;ant au milieu du peuple, ils dirent &agrave; J&eacute;sus: Ma&icirc;tre, cette femme a &eacute;t&eacute; surprise en flagrant d&eacute;lit d&#39;adult&egrave;re.</p>

<p><sup class="versenum">5&nbsp;</sup>Mo&iuml;se, dans la loi, nous a ordonn&eacute; de lapider de telles femmes: toi donc, que dis-tu?</p>

<p><sup class="versenum">6&nbsp;</sup>Ils disaient cela pour l&#39;&eacute;prouver, afin de pouvoir l&#39;accuser. Mais J&eacute;sus, s&#39;&eacute;tant baiss&eacute;, &eacute;crivait avec le doigt sur la terre.</p>

<p><sup class="versenum">7&nbsp;</sup>Comme ils continuaient &agrave; l&#39;interroger, il se releva et leur dit: Que celui de vous qui est sans p&eacute;ch&eacute; jette le premier la pierre contre elle.</p>

<p><sup class="versenum">8&nbsp;</sup>Et s&#39;&eacute;tant de nouveau baiss&eacute;, il &eacute;crivait sur la terre.</p>

<p><sup class="versenum">9&nbsp;</sup>Quand ils entendirent cela, accus&eacute;s par leur conscience, ils se retir&egrave;rent un &agrave; un, depuis les plus &acirc;g&eacute;s jusqu&#39;aux derniers; et J&eacute;sus resta seul avec la femme qui &eacute;tait l&agrave; au milieu.</p>

<p><sup class="versenum">10&nbsp;</sup>Alors s&#39;&eacute;tant relev&eacute;, et ne voyant plus que la femme, J&eacute;sus lui dit: Femme, o&ugrave; sont ceux qui t&#39;accusaient? Personne ne t&#39;a-t-il condamn&eacute;e?</p>

<p><sup class="versenum">11&nbsp;</sup>Elle r&eacute;pondit: Non, Seigneur. Et J&eacute;sus lui dit: Je ne te condamne pas non plus: va, et ne p&egrave;che plus.</p>
</div>
</div>
</div>
</div>
</div>
</div>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/241.mp4" type="button" class="external-movie">
         Regardez Jean 7:1-8:11 </button>
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

<p>J&eacute;sus et ses disciples sont all&eacute;s &agrave; J&eacute;rusalem pendant la saison d&#39;automne pour sept jours de F&ecirc;te des Tabernacles. C&#39;&eacute;tait un temps o&ugrave; tous les hommes juifs qui pouvaient le faire devaient se pr&eacute;senter &agrave; J&eacute;rusalem pour se faire connaitre. Les demi-fr&egrave;res de J&eacute;sus, qui ne croient toujours pas en lui, s&rsquo;en vont sans Lui. Plus tard, J&eacute;sus se pr&eacute;sente vers le milieu de la f&ecirc;te. Il va au temple pour enseigner qui Il est, le fils de David, encore &eacute;lev&eacute; &agrave; Nazareth. Une dispute &eacute;clate et il y a beaucoup de cris au sujet de J&eacute;sus, mais Il s&rsquo;est simplement retir&eacute; pour la nuit pour passer plus de temps avec le P&egrave;re. Les chefs religieux se disputaient au sujet de J&eacute;sus. Celui qui a r&eacute;cemment cru en J&eacute;sus a essay&eacute; d&#39;influencer le groupe mais ils l&#39;ont ridiculis&eacute;. Quand J&eacute;sus est revenu &agrave; J&eacute;rusalem, ils ont essay&eacute; de le pi&eacute;ger en lui pr&eacute;sentant une femme surprise dans l&#39;adult&egrave;re. J&eacute;sus exerce le mod&egrave;le de leadership avec beaucoup de sagesse, de compassion, de mis&eacute;ricorde et de gr&acirc;ce tout en mettant au d&eacute;fi les chefs religieux face &agrave; leur propre p&eacute;ch&eacute; et la duret&eacute; de leur c&oelig;ur.</p>

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

			<td class="social" @click="share('lesson', 'Leadership, Grâce et Compassion: ', '/content/M2/fra/multiply2/multiply241.html')">
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