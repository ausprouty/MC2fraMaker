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
                        <div class="chapter_number ltr"><h1>50.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership de la Résurrection</h1></div>
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
	<li>Lisez ou observez Jean 19:31-20:31 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 19:31-20</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<div>
<div>
<div>
<div>
<div>
<div>
<p><sup class="versenum">31&nbsp;</sup>Dans la crainte que les corps ne restassent sur la croix pendant le sabbat, -car c&#39;&eacute;tait la pr&eacute;paration, et ce jour de sabbat &eacute;tait un grand jour, -les Juifs demand&egrave;rent &agrave; Pilate qu&#39;on romp&icirc;t les jambes aux crucifi&eacute;s, et qu&#39;on les enlev&acirc;t.</p>

<p><sup class="versenum">32&nbsp;</sup>Les soldats vinrent donc, et ils rompirent les jambes au premier, puis &agrave; l&#39;autre qui avait &eacute;t&eacute; crucifi&eacute; avec lui.</p>

<p><sup class="versenum">33&nbsp;</sup>S&#39;&eacute;tant approch&eacute;s de J&eacute;sus, et le voyant d&eacute;j&agrave; mort, ils ne lui rompirent pas les jambes;</p>

<p><sup class="versenum">34&nbsp;</sup>mais un des soldats lui per&ccedil;a le c&ocirc;t&eacute; avec une lance, et aussit&ocirc;t il sortit du sang et de l&#39;eau.</p>

<p><sup class="versenum">35&nbsp;</sup>Celui qui l&#39;a vu en a rendu t&eacute;moignage, et son t&eacute;moignage est vrai; et il sait qu&#39;il dit vrai, afin que vous croyiez aussi.</p>

<p><sup class="versenum">36&nbsp;</sup>Ces choses sont arriv&eacute;es, afin que l&#39;&Eacute;criture f&ucirc;t accomplie: Aucun de ses os ne sera bris&eacute;.</p>

<p><sup class="versenum">37&nbsp;</sup>Et ailleurs l&#39;&Eacute;criture dit encore: Ils verront celui qu&#39;ils ont perc&eacute;.</p>

<p><sup class="versenum">38&nbsp;</sup>Apr&egrave;s cela, Joseph d&#39;Arimath&eacute;e, qui &eacute;tait disciple de J&eacute;sus, mais en secret par crainte des Juifs, demanda &agrave; Pilate la permission de prendre le corps de J&eacute;sus. Et Pilate le permit. Il vint donc, et prit le corps de J&eacute;sus.</p>

<p><sup class="versenum">39&nbsp;</sup>Nicod&egrave;me, qui auparavant &eacute;tait all&eacute; de nuit vers J&eacute;sus, vint aussi, apportant un m&eacute;lange d&#39;environ cent livres de myrrhe et d&#39;alo&egrave;s.</p>

<p><sup class="versenum">40&nbsp;</sup>Ils prirent donc le corps de J&eacute;sus, et l&#39;envelopp&egrave;rent de bandes, avec les aromates, comme c&#39;est la coutume d&#39;ensevelir chez les Juifs.</p>

<p><sup class="versenum">41&nbsp;</sup>Or, il y avait un jardin dans le lieu o&ugrave; J&eacute;sus avait &eacute;t&eacute; crucifi&eacute;, et dans le jardin un s&eacute;pulcre neuf, o&ugrave; personne encore n&#39;avait &eacute;t&eacute; mis.</p>

<p><sup class="versenum">42&nbsp;</sup>Ce fut l&agrave; qu&#39;ils d&eacute;pos&egrave;rent J&eacute;sus, &agrave; cause de la pr&eacute;paration des Juifs, parce que le s&eacute;pulcre &eacute;tait proche.</p>

<p><sup class="versenum">1 </sup>Le premier jour de la semaine, Marie de Magdala se rendit au s&eacute;pulcre d&egrave;s le matin, comme il faisait encore obscur; et elle vit que la pierre &eacute;tait &ocirc;t&eacute;e du s&eacute;pulcre.</p>

<p><sup class="versenum">2&nbsp;</sup>Elle courut vers Simon Pierre et vers l&#39;autre disciple que J&eacute;sus aimait, et leur dit: Ils ont enlev&eacute; du s&eacute;pulcre le Seigneur, et nous ne savons o&ugrave; ils l&#39;ont mis.</p>

<p><sup class="versenum">3&nbsp;</sup>Pierre et l&#39;autre disciple sortirent, et all&egrave;rent au s&eacute;pulcre.</p>

<p><sup class="versenum">4&nbsp;</sup>Ils couraient tous deux ensemble. Mais l&#39;autre disciple courut plus vite que Pierre, et arriva le premier au s&eacute;pulcre;</p>

<p><sup class="versenum">5&nbsp;</sup>s&#39;&eacute;tant baiss&eacute;, il vit les bandes qui &eacute;taient &agrave; terre, cependant il n&#39;entra pas.</p>

<p><sup class="versenum">6&nbsp;</sup>Simon Pierre, qui le suivait, arriva et entra dans le s&eacute;pulcre; il vit les bandes qui &eacute;taient &agrave; terre,</p>

<p><sup class="versenum">7&nbsp;</sup>et le linge qu&#39;on avait mis sur la t&ecirc;te de J&eacute;sus, non pas avec les bandes, mais pli&eacute; dans un lieu &agrave; part.</p>

<p><sup class="versenum">8&nbsp;</sup>Alors l&#39;autre disciple, qui &eacute;tait arriv&eacute; le premier au s&eacute;pulcre, entra aussi; et il vit, et il crut.</p>

<p><sup class="versenum">9&nbsp;</sup>Car ils ne comprenaient pas encore que, selon l&#39;&Eacute;criture, J&eacute;sus devait ressusciter des morts.</p>

<p><sup class="versenum">10&nbsp;</sup>Et les disciples s&#39;en retourn&egrave;rent chez eux.</p>

<p><sup class="versenum">11&nbsp;</sup>Cependant Marie se tenait dehors pr&egrave;s du s&eacute;pulcre, et pleurait. Comme elle pleurait, elle se baissa pour regarder dans le s&eacute;pulcre;</p>

<p><sup class="versenum">12&nbsp;</sup>et elle vit deux anges v&ecirc;tus de blanc, assis &agrave; la place o&ugrave; avait &eacute;t&eacute; couch&eacute; le corps de J&eacute;sus, l&#39;un &agrave; la t&ecirc;te, l&#39;autre aux pieds.</p>

<p><sup class="versenum">13&nbsp;</sup>Ils lui dirent: Femme, pourquoi pleures-tu? Elle leur r&eacute;pondit: Parce qu&#39;ils ont enlev&eacute; mon Seigneur, et je ne sais o&ugrave; ils l&#39;ont mis.</p>

<p><sup class="versenum">14&nbsp;</sup>En disant cela, elle se retourna, et elle vit J&eacute;sus debout; mais elle ne savait pas que c&#39;&eacute;tait J&eacute;sus.</p>

<p><sup class="versenum">15&nbsp;</sup>J&eacute;sus lui dit: Femme, pourquoi pleures-tu? Qui cherches-tu? Elle, pensant que c&#39;&eacute;tait le jardinier, lui dit: Seigneur, si c&#39;est toi qui l&#39;as emport&eacute;, dis-moi o&ugrave; tu l&#39;as mis, et je le prendrai.</p>

<p><sup class="versenum">16&nbsp;</sup>J&eacute;sus lui dit: Marie! Elle se retourna, et lui dit en h&eacute;breu: Rabbouni! c&#39;est-&agrave;-dire, Ma&icirc;tre!</p>

<p><sup class="versenum">17&nbsp;</sup>J&eacute;sus lui dit: Ne me touche pas; car je ne suis pas encore mont&eacute; vers mon P&egrave;re. Mais va trouver mes fr&egrave;res, et dis-leur que je monte vers mon P&egrave;re et votre P&egrave;re, vers mon Dieu et votre Dieu.</p>

<p><sup class="versenum">18&nbsp;</sup>Marie de Magdala alla annoncer aux disciples qu&#39;elle avait vu le Seigneur, et qu&#39;il lui avait dit ces choses.</p>

<p><sup class="versenum">19&nbsp;</sup>Le soir de ce jour, qui &eacute;tait le premier de la semaine, les portes du lieu o&ugrave; se trouvaient les disciples &eacute;tant ferm&eacute;es, &agrave; cause de la crainte qu&#39;ils avaient des Juifs, J&eacute;sus vint, se pr&eacute;senta au milieu d&#39;eux, et leur dit: La paix soit avec vous!</p>

<p><sup class="versenum">20&nbsp;</sup>Et quand il eut dit cela, il leur montra ses mains et son c&ocirc;t&eacute;. Les disciples furent dans la joie en voyant le Seigneur.</p>

<p><sup class="versenum">21&nbsp;</sup>J&eacute;sus leur dit de nouveau: La paix soit avec vous! Comme le P&egrave;re m&#39;a envoy&eacute;, moi aussi je vous envoie.</p>

<p><sup class="versenum">22&nbsp;</sup>Apr&egrave;s ces paroles, il souffla sur eux, et leur dit: Recevez le Saint Esprit.</p>

<p><sup class="versenum">23&nbsp;</sup>Ceux &agrave; qui vous pardonnerez les p&eacute;ch&eacute;s, ils leur seront pardonn&eacute;s; et ceux &agrave; qui vous les retiendrez, ils leur seront retenus.</p>

<p><sup class="versenum">24&nbsp;</sup>Thomas, appel&eacute; Didyme, l&#39;un des douze, n&#39;&eacute;tait pas avec eux lorsque J&eacute;sus vint.</p>

<p><sup class="versenum">25&nbsp;</sup>Les autres disciples lui dirent donc: Nous avons vu le Seigneur. Mais il leur dit: Si je ne vois dans ses mains la marque des clous, et si je ne mets mon doigt dans la marque des clous, et si je ne mets ma main dans son c&ocirc;t&eacute;, je ne croirai point.</p>

<p><sup class="versenum">26&nbsp;</sup>Huit jours apr&egrave;s, les disciples de J&eacute;sus &eacute;taient de nouveau dans la maison, et Thomas se trouvait avec eux. J&eacute;sus vint, les portes &eacute;tant ferm&eacute;es, se pr&eacute;senta au milieu d&#39;eux, et dit: La paix soit avec vous!</p>

<p><sup class="versenum">27&nbsp;</sup>Puis il dit &agrave; Thomas: Avance ici ton doigt, et regarde mes mains; avance aussi ta main, et mets-la dans mon c&ocirc;t&eacute;; et ne sois pas incr&eacute;dule, mais crois.</p>

<p><sup class="versenum">28&nbsp;</sup>Thomas lui r&eacute;pondit: Mon Seigneur et mon Dieu! J&eacute;sus lui dit:</p>

<p><sup class="versenum">29&nbsp;</sup>Parce que tu m&#39;as vu, tu as cru. Heureux ceux qui n&#39;ont pas vu, et qui ont cru!</p>

<p><sup class="versenum">30&nbsp;</sup>J&eacute;sus a fait encore, en pr&eacute;sence de ses disciples, beaucoup d&#39;autres miracles, qui ne sont pas &eacute;crits dans ce livre.</p>

<p><sup class="versenum">31&nbsp;</sup>Mais ces choses ont &eacute;t&eacute; &eacute;crites afin que vous croyiez que J&eacute;sus est le Christ, le Fils de Dieu, et qu&#39;en croyant vous ayez la vie en son nom.</p>
</div>
</div>
</div>
</div>
</div>
</div>
<!-- end bible -->

<p class="bible"></p>

<p>&nbsp;</p>
<!-- begin bible -->

</div>

<button id="MC2/fra/video/multiply2/250.mp4" type="button" class="external-movie">
         Regardez Jean 19:31-20 </button>
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

<p>IL est ressuscit&eacute; des morts! La Bible dit que la r&eacute;surrection de J&eacute;sus a chang&eacute; toutes choses. &laquo; Or, si nous sommes morts avec Christ, nous croyons que nous vivrons aussi avec lui, sachant que Christ ressuscit&eacute; des morts ne meurt plus ; la mort n&rsquo;a plus de pouvoir sur lui. Car il est mort, et c&rsquo;est pour le p&eacute;ch&eacute; qu&rsquo;il est mort une fois pour toutes ; il est revenu &agrave; la vie, et c&rsquo;est pour Dieu qu&rsquo;il vit. &raquo; (Romains 6:8-11). Le pouvoir de vivre r&eacute;side dans le pouvoir de la victoire de J&eacute;sus sur la mort. La r&eacute;surrection de J&eacute;sus nous donne le pouvoir de vaincre le p&eacute;ch&eacute; dans nos vies pendant que nous nous abandonnons &agrave; l&#39;&oelig;uvre transformatrice du P&egrave;re. La puissance de J&eacute;sus et sa r&eacute;surrection circulent &agrave; travers nous pendant que nous mettons de c&ocirc;t&eacute; notre volont&eacute; et permettons &agrave; J&eacute;sus de vivre en nous et &agrave; travers nous. Le leadership de la r&eacute;surrection est un leadership qui permet &agrave; J&eacute;sus de vivre en et &agrave; travers soi. Conduire comme J&eacute;sus est radicalement diff&eacute;rent du leadership mondain qui cherche &agrave; se promouvoir et &agrave; contr&ocirc;ler les autres.</p>

<ul>
	<li class="nobreak-final-final">Pour une &eacute;tude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Luc 23:50-24:49</span>;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<div>
	<div>
	<div>
	<div>
	<div>
	<div>
	<p><sup class="versenum">50&nbsp;</sup>Il y avait un conseiller, nomm&eacute; Joseph, homme bon et juste,</p>

	<p><sup class="versenum">51&nbsp;</sup>qui n&#39;avait point particip&eacute; &agrave; la d&eacute;cision et aux actes des autres; il &eacute;tait d&#39;Arimath&eacute;e, ville des Juifs, et il attendait le royaume de Dieu.</p>

	<p><sup class="versenum">52&nbsp;</sup>Cet homme se rendit vers Pilate, et demanda le corps de J&eacute;sus.</p>

	<p><sup class="versenum">53&nbsp;</sup>Il le descendit de la croix, l&#39;enveloppa d&#39;un linceul, et le d&eacute;posa dans un s&eacute;pulcre taill&eacute; dans le roc, o&ugrave; personne n&#39;avait encore &eacute;t&eacute; mis.</p>

	<p><sup class="versenum">54&nbsp;</sup>C&#39;&eacute;tait le jour de la pr&eacute;paration, et le sabbat allait commencer.</p>

	<p><sup class="versenum">55&nbsp;</sup>Les femmes qui &eacute;taient venues de la Galil&eacute;e avec J&eacute;sus accompagn&egrave;rent Joseph, virent le s&eacute;pulcre et la mani&egrave;re dont le corps de J&eacute;sus y fut d&eacute;pos&eacute;,</p>

	<p><sup class="versenum">56&nbsp;</sup>et, s&#39;en &eacute;tant retourn&eacute;es, elles pr&eacute;par&egrave;rent des aromates et des parfums. Puis elles se repos&egrave;rent le jour du sabbat, selon la loi.</p>

	<p><sup class="versenum">1 </sup>Le premier jour de la semaine, elles se rendirent au s&eacute;pulcre de grand matin, portant les aromates qu&#39;elles avaient pr&eacute;par&eacute;s.</p>

	<p><sup class="versenum">2&nbsp;</sup>Elles trouv&egrave;rent que la pierre avait &eacute;t&eacute; roul&eacute;e de devant le s&eacute;pulcre;</p>

	<p><sup class="versenum">3&nbsp;</sup>et, &eacute;tant entr&eacute;es, elles ne trouv&egrave;rent pas le corps du Seigneur J&eacute;sus.</p>

	<p><sup class="versenum">4&nbsp;</sup>Comme elles ne savaient que penser de cela, voici, deux hommes leur apparurent, en habits resplendissants.</p>

	<p><sup class="versenum">5&nbsp;</sup>Saisies de frayeur, elles baiss&egrave;rent le visage contre terre; mais ils leur dirent: Pourquoi cherchez-vous parmi les morts celui qui est vivant?</p>

	<p><sup class="versenum">6&nbsp;</sup>Il n&#39;est point ici, mais il est ressuscit&eacute;. Souvenez-vous de quelle mani&egrave;re il vous a parl&eacute;, lorsqu&#39;il &eacute;tait encore en Galil&eacute;e,</p>

	<p><sup class="versenum">7&nbsp;</sup>et qu&#39;il disait: Il faut que le Fils de l&#39;homme soit livr&eacute; entre les mains des p&eacute;cheurs, qu&#39;il soit crucifi&eacute;, et qu&#39;il ressuscite le troisi&egrave;me jour.</p>

	<p><sup class="versenum">8&nbsp;</sup>Et elles se ressouvinrent des paroles de J&eacute;sus.</p>

	<p><sup class="versenum">9&nbsp;</sup>A leur retour du s&eacute;pulcre, elles annonc&egrave;rent toutes ces choses aux onze, et &agrave; tous les autres.</p>

	<p><sup class="versenum">10&nbsp;</sup>Celles qui dirent ces choses aux ap&ocirc;tres &eacute;taient Marie de Magdala, Jeanne, Marie, m&egrave;re de Jacques, et les autres qui &eacute;taient avec elles.</p>

	<p><sup class="versenum">11&nbsp;</sup>Ils tinrent ces discours pour des r&ecirc;veries, et ils ne crurent pas ces femmes.</p>

	<p><sup class="versenum">12&nbsp;</sup>Mais Pierre se leva, et courut au s&eacute;pulcre. S&#39;&eacute;tant baiss&eacute;, il ne vit que les linges qui &eacute;taient &agrave; terre; puis il s&#39;en alla chez lui, dans l&#39;&eacute;tonnement de ce qui &eacute;tait arriv&eacute;.</p>

	<p><sup class="versenum">13&nbsp;</sup>Et voici, ce m&ecirc;me jour, deux disciples allaient &agrave; un village nomm&eacute; Emma&uuml;s, &eacute;loign&eacute; de J&eacute;rusalem de soixante stades;</p>

	<p><sup class="versenum">14&nbsp;</sup>et ils s&#39;entretenaient de tout ce qui s&#39;&eacute;tait pass&eacute;.</p>

	<p><sup class="versenum">15&nbsp;</sup>Pendant qu&#39;ils parlaient et discutaient, J&eacute;sus s&#39;approcha, et fit route avec eux.</p>

	<p><sup class="versenum">16&nbsp;</sup>Mais leurs yeux &eacute;taient emp&ecirc;ch&eacute;s de le reconna&icirc;tre.</p>

	<p><sup class="versenum">17&nbsp;</sup>Il leur dit: De quoi vous entretenez-vous en marchant, pour que vous soyez tout tristes?</p>

	<p><sup class="versenum">18&nbsp;</sup>L&#39;un d&#39;eux, nomm&eacute; Cl&eacute;opas, lui r&eacute;pondit: Es-tu le seul qui, s&eacute;journant &agrave; J&eacute;rusalem ne sache pas ce qui y est arriv&eacute; ces jours-ci? -</p>

	<p><sup class="versenum">19&nbsp;</sup>Quoi? leur dit-il. -Et ils lui r&eacute;pondirent: Ce qui est arriv&eacute; au sujet de J&eacute;sus de Nazareth, qui &eacute;tait un proph&egrave;te puissant en oeuvres et en paroles devant Dieu et devant tout le peuple,</p>

	<p><sup class="versenum">20&nbsp;</sup>et comment les principaux sacrificateurs et nos magistrats l&#39;on livr&eacute; pour le faire condamner &agrave; mort et l&#39;ont crucifi&eacute;.</p>

	<p><sup class="versenum">21&nbsp;</sup>Nous esp&eacute;rions que ce serait lui qui d&eacute;livrerait Isra&euml;l; mais avec tout cela, voici le troisi&egrave;me jour que ces choses se sont pass&eacute;es.</p>

	<p><sup class="versenum">22&nbsp;</sup>Il est vrai que quelques femmes d&#39;entre nous nous ont fort &eacute;tonn&eacute;s; s&#39;&eacute;tant rendues de grand matin au s&eacute;pulcre</p>

	<p><sup class="versenum">23&nbsp;</sup>et n&#39;ayant pas trouv&eacute; son corps, elles sont venues dire que des anges leurs sont apparus et ont annonc&eacute; qu&#39;il est vivant.</p>

	<p><sup class="versenum">24&nbsp;</sup>Quelques-uns de ceux qui &eacute;taient avec nous sont all&eacute;s au s&eacute;pulcre, et ils ont trouv&eacute; les choses comme les femmes l&#39;avaient dit; mais lui, ils ne l&#39;ont point vu.</p>

	<p><sup class="versenum">25&nbsp;</sup>Alors J&eacute;sus leur dit: O hommes sans intelligence, et dont le coeur est lent &agrave; croire tout ce qu&#39;ont dit les proph&egrave;tes!</p>

	<p><sup class="versenum">26&nbsp;</sup>Ne fallait-il pas que le Christ souffr&icirc;t ces choses, et qu&#39;il entr&acirc;t dans sa gloire?</p>

	<p><sup class="versenum">27&nbsp;</sup>Et, commen&ccedil;ant par Mo&iuml;se et par tous les proph&egrave;tes, il leur expliqua dans toutes les &Eacute;critures ce qui le concernait.</p>

	<p><sup class="versenum">28&nbsp;</sup>Lorsqu&#39;ils furent pr&egrave;s du village o&ugrave; ils allaient, il parut vouloir aller plus loin.</p>

	<p><sup class="versenum">29&nbsp;</sup>Mais ils le press&egrave;rent, en disant: Reste avec nous, car le soir approche, le jour est sur son d&eacute;clin. Et il entra, pour rester avec eux.</p>

	<p><sup class="versenum">30&nbsp;</sup>Pendant qu&#39;il &eacute;tait &agrave; table avec eux, il prit le pain; et, apr&egrave;s avoir rendu gr&acirc;ces, il le rompit, et le leur donna.</p>

	<p><sup class="versenum">31&nbsp;</sup>Alors leurs yeux s&#39;ouvrirent, et ils le reconnurent; mais il disparut de devant eux.</p>

	<p><sup class="versenum">32&nbsp;</sup>Et ils se dirent l&#39;un &agrave; l&#39;autre: Notre coeur ne br&ucirc;lait-il pas au dedans de nous, lorsqu&#39;il nous parlait en chemin et nous expliquait les &Eacute;critures?</p>

	<p><sup class="versenum">33&nbsp;</sup>Se levant &agrave; l&#39;heure m&ecirc;me, ils retourn&egrave;rent &agrave; J&eacute;rusalem, et ils trouv&egrave;rent les onze, et ceux qui &eacute;taient avec eux, assembl&eacute;s</p>

	<p><sup class="versenum">34&nbsp;</sup>et disant: Le Seigneur est r&eacute;ellement ressuscit&eacute;, et il est apparu &agrave; Simon.</p>

	<p><sup class="versenum">35&nbsp;</sup>Et ils racont&egrave;rent ce qui leur &eacute;tait arriv&eacute; en chemin, et comment ils l&#39;avaient reconnu au moment o&ugrave; il rompit le pain.</p>

	<p><sup class="versenum">36&nbsp;</sup>Tandis qu&#39;ils parlaient de la sorte, lui-m&ecirc;me se pr&eacute;senta au milieu d&#39;eux, et leur dit: La paix soit avec vous!</p>

	<p><sup class="versenum">37&nbsp;</sup>Saisis de frayeur et d&#39;&eacute;pouvante, ils croyaient voir un esprit.</p>

	<p><sup class="versenum">38&nbsp;</sup>Mais il leur dit: Pourquoi &ecirc;tes-vous troubl&eacute;s, et pourquoi pareilles pens&eacute;es s&#39;&eacute;l&egrave;vent-elles dans vos coeurs?</p>

	<p><sup class="versenum">39&nbsp;</sup>Voyez mes mains et mes pieds, c&#39;est bien moi; touchez-moi et voyez: un esprit n&#39;a ni chair ni os, comme vous voyez que j&#39;ai.</p>

	<p><sup class="versenum">40&nbsp;</sup>Et en disant cela, il leur montra ses mains et ses pieds.</p>

	<p><sup class="versenum">41&nbsp;</sup>Comme, dans leur joie, ils ne croyaient point encore, et qu&#39;ils &eacute;taient dans l&#39;&eacute;tonnement, il leur dit: Avez-vous ici quelque chose &agrave; manger?</p>

	<p><sup class="versenum">42&nbsp;</sup>Ils lui pr&eacute;sent&egrave;rent du poisson r&ocirc;ti et un rayon de miel.</p>

	<p><sup class="versenum">43&nbsp;</sup>Il en prit, et il mangea devant eux.</p>

	<p><sup class="versenum">44&nbsp;</sup>Puis il leur dit: C&#39;est l&agrave; ce que je vous disais lorsque j&#39;&eacute;tais encore avec vous, qu&#39;il fallait que s&#39;accompl&icirc;t tout ce qui est &eacute;crit de moi dans la loi de Mo&iuml;se, dans les proph&egrave;tes, et dans les psaumes.</p>

	<p><sup class="versenum">45&nbsp;</sup>Alors il leur ouvrit l&#39;esprit, afin qu&#39;ils comprissent les &Eacute;critures.</p>

	<p><sup class="versenum">46&nbsp;</sup>Et il leur dit: Ainsi il est &eacute;crit que le Christ souffrirait, et qu&#39;il ressusciterait des morts le troisi&egrave;me jour,</p>

	<p><sup class="versenum">47&nbsp;</sup>et que la repentance et le pardon des p&eacute;ch&eacute;s seraient pr&ecirc;ch&eacute;s en son nom &agrave; toutes les nations, &agrave; commencer par J&eacute;rusalem.</p>

	<p><sup class="versenum">48&nbsp;</sup>Vous &ecirc;tes t&eacute;moins de ces choses.</p>

	<p><sup class="versenum">49&nbsp;</sup>Et voici, j&#39;enverrai sur vous ce que mon P&egrave;re a promis; mais vous, restez dans la ville jusqu&#39;&agrave; ce que vous soyez rev&ecirc;tus de la puissance d&#39;en haut.</p>
	</div>
	</div>
	</div>
	</div>
	</div>
	</div>
	<!-- end bible --></div>
	&nbsp;<span class="popup-link" @click = "popUp('pop2')"> Matthieu 27:57-28:15</span>;&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<div>
	<div>
	<div>
	<div>
	<div>
	<div>
	<p><sup class="versenum">57&nbsp;</sup>Le soir &eacute;tant venu, arriva un homme riche d&#39;Arimath&eacute;e, nomm&eacute; Joseph, lequel &eacute;tait aussi disciple de J&eacute;sus.</p>

	<p><sup class="versenum">58&nbsp;</sup>Il se rendit vers Pilate, et demanda le corps de J&eacute;sus. Et Pilate ordonna de le remettre.</p>

	<p><sup class="versenum">59&nbsp;</sup>Joseph prit le corps, l&#39;enveloppa d&#39;un linceul blanc,</p>

	<p><sup class="versenum">60&nbsp;</sup>et le d&eacute;posa dans un s&eacute;pulcre neuf, qu&#39;il s&#39;&eacute;tait fait tailler dans le roc. Puis il roula une grande pierre &agrave; l&#39;entr&eacute;e du s&eacute;pulcre, et il s&#39;en alla.</p>

	<p><sup class="versenum">61&nbsp;</sup>Marie de Magdala et l&#39;autre Marie &eacute;taient l&agrave;, assises vis-&agrave;-vis du s&eacute;pulcre.</p>

	<p><sup class="versenum">62&nbsp;</sup>Le lendemain, qui &eacute;tait le jour apr&egrave;s la pr&eacute;paration, les principaux sacrificateurs et les pharisiens all&egrave;rent ensemble aupr&egrave;s de Pilate,</p>

	<p><sup class="versenum">63&nbsp;</sup>et dirent: Seigneur, nous nous souvenons que cet imposteur a dit, quand il vivait encore: Apr&egrave;s trois jours je ressusciterai.</p>

	<p><sup class="versenum">64&nbsp;</sup>Ordonne donc que le s&eacute;pulcre soit gard&eacute; jusqu&#39;au troisi&egrave;me jour, afin que ses disciples ne viennent pas d&eacute;rober le corps, et dire au peuple: Il est ressuscit&eacute; des morts. Cette derni&egrave;re imposture serait pire que la premi&egrave;re.</p>

	<p><sup class="versenum">65&nbsp;</sup>Pilate leur dit: Vous avez une garde; allez, gardez-le comme vous l&#39;entendrez.</p>

	<p><sup class="versenum">66&nbsp;</sup>Ils s&#39;en all&egrave;rent, et s&#39;assur&egrave;rent du s&eacute;pulcre au moyen de la garde, apr&egrave;s avoir scell&eacute; la pierre.</p>

	<p><sup class="versenum">1 </sup>Apr&egrave;s le sabbat, &agrave; l&#39;aube du premier jour de la semaine, Marie de Magdala et l&#39;autre Marie all&egrave;rent voir le s&eacute;pulcre.</p>

	<p><sup class="versenum">2&nbsp;</sup>Et voici, il y eut un grand tremblement de terre; car un ange du Seigneur descendit du ciel, vint rouler la pierre, et s&#39;assit dessus.</p>

	<p><sup class="versenum">3&nbsp;</sup>Son aspect &eacute;tait comme l&#39;&eacute;clair, et son v&ecirc;tement blanc comme la neige.</p>

	<p><sup class="versenum">4&nbsp;</sup>Les gardes trembl&egrave;rent de peur, et devinrent comme morts.</p>

	<p><sup class="versenum">5&nbsp;</sup>Mais l&#39;ange prit la parole, et dit aux femmes: Pour vous, ne craignez pas; car je sais que vous cherchez J&eacute;sus qui a &eacute;t&eacute; crucifi&eacute;.</p>

	<p><sup class="versenum">6&nbsp;</sup>Il n&#39;est point ici; il est ressuscit&eacute;, comme il l&#39;avait dit. Venez, voyez le lieu o&ugrave; il &eacute;tait couch&eacute;,</p>

	<p><sup class="versenum">7&nbsp;</sup>et allez promptement dire &agrave; ses disciples qu&#39;il est ressuscit&eacute; des morts. Et voici, il vous pr&eacute;c&egrave;de en Galil&eacute;e: c&#39;est l&agrave; que vous le verrez. Voici, je vous l&#39;ai dit.</p>

	<p><sup class="versenum">8&nbsp;</sup>Elles s&#39;&eacute;loign&egrave;rent promptement du s&eacute;pulcre, avec crainte et avec une grande joie, et elles coururent porter la nouvelle aux disciples.</p>

	<p><sup class="versenum">9&nbsp;</sup>Et voici, J&eacute;sus vint &agrave; leur rencontre, et dit: Je vous salue. Elles s&#39;approch&egrave;rent pour saisir ses pieds, et elles se prostern&egrave;rent devant lui.</p>

	<p><sup class="versenum">10&nbsp;</sup>Alors J&eacute;sus leur dit: Ne craignez pas; allez dire &agrave; mes fr&egrave;res de se rendre en Galil&eacute;e: c&#39;est l&agrave; qu&#39;ils me verront.</p>

	<p><sup class="versenum">11&nbsp;</sup>Pendant qu&#39;elles &eacute;taient en chemin, quelques hommes de la garde entr&egrave;rent dans la ville, et annonc&egrave;rent aux principaux sacrificateurs tout ce qui &eacute;tait arriv&eacute;.</p>

	<p><sup class="versenum">12&nbsp;</sup>Ceux-ci, apr&egrave;s s&#39;&ecirc;tre assembl&eacute;s avec les anciens et avoir tenu conseil, donn&egrave;rent aux soldats une forte somme d&#39;argent,</p>

	<p><sup class="versenum">13&nbsp;</sup>en disant: Dites: Ses disciples sont venus de nuit le d&eacute;rober, pendant que nous dormions.</p>

	<p><sup class="versenum">14&nbsp;</sup>Et si le gouverneur l&#39;apprend, nous l&#39;apaiserons, et nous vous tirerons de peine.</p>

	<p><sup class="versenum">15&nbsp;</sup>Les soldats prirent l&#39;argent, et suivirent les instructions qui leur furent donn&eacute;es. Et ce bruit s&#39;est r&eacute;pandu parmi les Juifs, jusqu&#39;&agrave; ce jour.</p>
	</div>
	</div>
	</div>
	</div>
	</div>
	</div>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop3')"> Marc 15:42- 16:18</span>.

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<div>
	<div>
	<div>
	<div>
	<div>
	<div>
	<p><sup class="versenum">42&nbsp;</sup>Le soir &eacute;tant venu, comme c&#39;&eacute;tait la pr&eacute;paration, c&#39;est-&agrave;-dire, la veille du sabbat, -</p>

	<p><sup class="versenum">43&nbsp;</sup>arriva Joseph d&#39;Arimath&eacute;e, conseiller de distinction, qui lui-m&ecirc;me attendait aussi le royaume de Dieu. Il osa se rendre vers Pilate, pour demander le corps de J&eacute;sus.</p>

	<p><sup class="versenum">44&nbsp;</sup>Pilate s&#39;&eacute;tonna qu&#39;il f&ucirc;t mort si t&ocirc;t; fit venir le centenier et lui demanda s&#39;il &eacute;tait mort depuis longtemps.</p>

	<p><sup class="versenum">45&nbsp;</sup>S&#39;en &eacute;tant assur&eacute; par le centenier, il donna le corps &agrave; Joseph.</p>

	<p><sup class="versenum">46&nbsp;</sup>Et Joseph, ayant achet&eacute; un linceul, descendit J&eacute;sus de la croix, l&#39;enveloppa du linceul, et le d&eacute;posa dans un s&eacute;pulcre taill&eacute; dans le roc. Puis il roula une pierre &agrave; l&#39;entr&eacute;e du s&eacute;pulcre.</p>

	<p><sup class="versenum">47&nbsp;</sup>Marie de Magdala, et Marie, m&egrave;re de Joses, regardaient o&ugrave; on le mettait.</p>

	<p><sup class="versenum">1 </sup>Lorsque le sabbat fut pass&eacute;, Marie de Magdala, Marie, m&egrave;re de Jacques, et Salom&eacute;, achet&egrave;rent des aromates, afin d&#39;aller embaumer J&eacute;sus.</p>

	<p><sup class="versenum">2&nbsp;</sup>Le premier jour de la semaine, elles se rendirent au s&eacute;pulcre, de grand matin, comme le soleil venait de se lever.</p>

	<p><sup class="versenum">3&nbsp;</sup>Elles disaient entre elles: Qui nous roulera la pierre loin de l&#39;entr&eacute;e du s&eacute;pulcre?</p>

	<p><sup class="versenum">4&nbsp;</sup>Et, levant les yeux, elles aper&ccedil;urent que la pierre, qui &eacute;tait tr&egrave;s grande, avait &eacute;t&eacute; roul&eacute;e.</p>

	<p><sup class="versenum">5&nbsp;</sup>Elles entr&egrave;rent dans le s&eacute;pulcre, virent un jeune homme assis &agrave; droite v&ecirc;tu d&#39;une robe blanche, et elles furent &eacute;pouvant&eacute;es.</p>

	<p><sup class="versenum">6&nbsp;</sup>Il leur dit: Ne vous &eacute;pouvantez pas; vous cherchez J&eacute;sus de Nazareth, qui a &eacute;t&eacute; crucifi&eacute;; il est ressuscit&eacute;, il n&#39;est point ici; voici le lieu o&ugrave; on l&#39;avait mis.</p>

	<p><sup class="versenum">7&nbsp;</sup>Mais allez dire &agrave; ses disciples et &agrave; Pierre qu&#39;il vous pr&eacute;c&egrave;de en Galil&eacute;e: c&#39;est l&agrave; que vous le verrez, comme il vous l&#39;a dit.</p>

	<p><sup class="versenum">8&nbsp;</sup>Elles sortirent du s&eacute;pulcre et s&#39;enfuirent. La peur et le trouble les avaient saisies; et elles ne dirent rien &agrave; personne, &agrave; cause de leur effroi.</p>

	<p><sup class="versenum">9&nbsp;</sup>J&eacute;sus, &eacute;tant ressuscit&eacute; le matin du premier jour de la semaine, apparut d&#39;abord &agrave; Marie de Magdala, de laquelle il avait chass&eacute; sept d&eacute;mons.</p>

	<p><sup class="versenum">10&nbsp;</sup>Elle alla en porter la nouvelle &agrave; ceux qui avaient &eacute;t&eacute; avec lui, et qui s&#39;affligeaient et pleuraient.</p>

	<p><sup class="versenum">11&nbsp;</sup>Quand ils entendirent qu&#39;il vivait, et qu&#39;elle l&#39;avait vu, ils ne le crurent point.</p>

	<p><sup class="versenum">12&nbsp;</sup>Apr&egrave;s cela, il apparut, sous une autre forme, &agrave; deux d&#39;entre eux qui &eacute;taient en chemin pour aller &agrave; la campagne.</p>

	<p><sup class="versenum">13&nbsp;</sup>Ils revinrent l&#39;annoncer aux autres, qui ne les crurent pas non plus.</p>

	<p><sup class="versenum">14&nbsp;</sup>Enfin, il apparut aux onze, pendant qu&#39;ils &eacute;taient &agrave; table; et il leur reprocha leur incr&eacute;dulit&eacute; et la duret&eacute; de leur coeur, parce qu&#39;ils n&#39;avaient pas cru ceux qui l&#39;avaient vu ressuscit&eacute;.</p>

	<p><sup class="versenum">15&nbsp;</sup>Puis il leur dit: Allez par tout le monde, et pr&ecirc;chez la bonne nouvelle &agrave; toute la cr&eacute;ation.</p>

	<p><sup class="versenum">16&nbsp;</sup>Celui qui croira et qui sera baptis&eacute; sera sauv&eacute;, mais celui qui ne croira pas sera condamn&eacute;.</p>

	<p><sup class="versenum">17&nbsp;</sup>Voici les miracles qui accompagneront ceux qui auront cru: en mon nom, ils chasseront les d&eacute;mons; ils parleront de nouvelles langues;</p>

	<p><sup class="versenum">18&nbsp;</sup>ils saisiront des serpents; s&#39;ils boivent quelque breuvage mortel, il ne leur feront point de mal; ils imposeront les mains aux malades, et les malades, seront gu&eacute;ris.</p>
	</div>
	</div>
	</div>
	</div>
	</div>
	</div>
	<!-- end bible --></div>
	.</li>
</ul>

</div>

<p class="enrichment">&nbsp;</p>

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

			<td class="social" @click="share('lesson', 'Leadership de la Résurrection: ', '/content/M2/fra/multiply2/multiply250.html')">
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