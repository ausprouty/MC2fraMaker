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
                        <div class="chapter_number ltr"><h1>4.</h1></div>
                        <div class="chapter_title ltr"><h1>Pierre s'adresse à la foule</h1></div>
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
	</div>
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
	<li>Lisez ou observez Actes 2:14-41 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 2:14-41</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">14&nbsp;</sup>Alors Pierre, se pr&eacute;sentant avec les onze, &eacute;leva la voix, et leur parla en ces termes: Hommes Juifs, et vous tous qui s&eacute;journez &agrave; J&eacute;rusalem, sachez ceci, et pr&ecirc;tez l&#39;oreille &agrave; mes paroles!</p>

<p><sup class="versenum">15&nbsp;</sup>Ces gens ne sont pas ivres, comme vous le supposez, car c&#39;est la troisi&egrave;me heure du jour.</p>

<p><sup class="versenum">16&nbsp;</sup>Mais c&#39;est ici ce qui a &eacute;t&eacute; dit par le proph&egrave;te Jo&euml;l:</p>

<p><sup class="versenum">17&nbsp;</sup>Dans les derniers jours, dit Dieu, je r&eacute;pandrai de mon Esprit sur toute chair; Vos fils et vos filles proph&eacute;tiseront, Vos jeunes gens auront des visions, Et vos vieillards auront des songes.</p>

<p><sup class="versenum">18&nbsp;</sup>Oui, sur mes serviteurs et sur mes servantes, Dans ces jours-l&agrave;, je r&eacute;pandrai de mon Esprit; et ils proph&eacute;tiseront.</p>

<p><sup class="versenum">19&nbsp;</sup>Je ferai para&icirc;tre des prodiges en haut dans le ciel et des miracles en bas sur la terre, Du sang, du feu, et une vapeur de fum&eacute;e;</p>

<p><sup class="versenum">20&nbsp;</sup>Le soleil se changera en t&eacute;n&egrave;bres, Et la lune en sang, Avant l&#39;arriv&eacute;e du jour du Seigneur, De ce jour grand et glorieux.</p>

<p><sup class="versenum">21&nbsp;</sup>Alors quiconque invoquera le nom du Seigneur sera sauv&eacute;.</p>

<p><sup class="versenum">22&nbsp;</sup>Hommes Isra&eacute;lites, &eacute;coutez ces paroles! J&eacute;sus de Nazareth, cet homme &agrave; qui Dieu a rendu t&eacute;moignage devant vous par les miracles, les prodiges et les signes qu&#39;il a op&eacute;r&eacute;s par lui au milieu de vous, comme vous le savez vous-m&ecirc;mes;</p>

<p><sup class="versenum">23&nbsp;</sup>cet homme, livr&eacute; selon le dessein arr&ecirc;t&eacute; et selon la prescience de Dieu, vous l&#39;avez crucifi&eacute;, vous l&#39;avez fait mourir par la main des impies.</p>

<p><sup class="versenum">24&nbsp;</sup>Dieu l&#39;a ressuscit&eacute;, en le d&eacute;livrant des liens de la mort, parce qu&#39;il n&#39;&eacute;tait pas possible qu&#39;il f&ucirc;t retenu par elle.</p>

<p><sup class="versenum">25&nbsp;</sup>Car David dit de lui: Je voyais constamment le Seigneur devant moi, Parce qu&#39;il est &agrave; ma droite, afin que je ne sois point &eacute;branl&eacute;.</p>

<p><sup class="versenum">26&nbsp;</sup>Aussi mon coeur est dans la joie, et ma langue dans l&#39;all&eacute;gresse; Et m&ecirc;me ma chair reposera avec esp&eacute;rance,</p>

<p><sup class="versenum">27&nbsp;</sup>Car tu n&#39;abandonneras pas mon &acirc;me dans le s&eacute;jour des morts, Et tu ne permettras pas que ton Saint voie la corruption.</p>

<p><sup class="versenum">28&nbsp;</sup>Tu m&#39;as fait conna&icirc;tre les sentiers de la vie, Tu me rempliras de joie par ta pr&eacute;sence.</p>

<p><sup class="versenum">29&nbsp;</sup>Hommes fr&egrave;res, qu&#39;il me soit permis de vous dire librement, au sujet du patriarche David, qu&#39;il est mort, qu&#39;il a &eacute;t&eacute; enseveli, et que son s&eacute;pulcre existe encore aujourd&#39;hui parmi nous.</p>

<p><sup class="versenum">30&nbsp;</sup>Comme il &eacute;tait proph&egrave;te, et qu&#39;il savait que Dieu lui avait promis avec serment de faire asseoir un de ses descendants sur son tr&ocirc;ne,</p>

<p><sup class="versenum">31&nbsp;</sup>c&#39;est la r&eacute;surrection du Christ qu&#39;il a pr&eacute;vue et annonc&eacute;e, en disant qu&#39;il ne serait pas abandonn&eacute; dans le s&eacute;jour des morts et que sa chair ne verrait pas la corruption.</p>

<p><sup class="versenum">32&nbsp;</sup>C&#39;est ce J&eacute;sus que Dieu a ressuscit&eacute;; nous en sommes tous t&eacute;moins.</p>

<p><sup class="versenum">33&nbsp;</sup>&Eacute;lev&eacute; par la droite de Dieu, il a re&ccedil;u du P&egrave;re le Saint Esprit qui avait &eacute;t&eacute; promis, et il l&#39;a r&eacute;pandu, comme vous le voyez et l&#39;entendez.</p>

<p><sup class="versenum">34&nbsp;</sup>Car David n&#39;est point mont&eacute; au ciel, mais il dit lui-m&ecirc;me: Le Seigneur a dit &agrave; mon Seigneur: Assieds-toi &agrave; ma droite,</p>

<p><sup class="versenum">35&nbsp;</sup>Jusqu&#39;&agrave; ce que je fasse de tes ennemis ton marchepied.</p>

<p><sup class="versenum">36&nbsp;</sup>Que toute la maison d&#39;Isra&euml;l sache donc avec certitude que Dieu a fait Seigneur et Christ ce J&eacute;sus que vous avez crucifi&eacute;.</p>

<p><sup class="versenum">37&nbsp;</sup>Apr&egrave;s avoir entendu ce discours, ils eurent le coeur vivement touch&eacute;, et ils dirent &agrave; Pierre et aux autres ap&ocirc;tres: Hommes fr&egrave;res, que ferons-nous?</p>

<p><sup class="versenum">38&nbsp;</sup>Pierre leur dit: Repentez-vous, et que chacun de vous soit baptis&eacute; au nom de J&eacute;sus Christ, pour le pardon de vos p&eacute;ch&eacute;s; et vous recevrez le don du Saint Esprit.</p>

<p><sup class="versenum">39&nbsp;</sup>Car la promesse est pour vous, pour vos enfants, et pour tous ceux qui sont au loin, en aussi grand nombre que le Seigneur notre Dieu les appellera.</p>

<p><sup class="versenum">40&nbsp;</sup>Et, par plusieurs autres paroles, il les conjurait et les exhortait, disant: Sauvez-vous de cette g&eacute;n&eacute;ration perverse.</p>

<p><sup class="versenum">41&nbsp;</sup>Ceux qui accept&egrave;rent sa parole furent baptis&eacute;s; et, en ce jour-l&agrave;, le nombre des disciples s&#39;augmenta d&#39;environ trois mille &acirc;mes.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/304.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 2:14-41&nbsp; </button>
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
	<li class="nobreak-final-final">Il y a seulement quelques semaines plus t&ocirc;t, J&eacute;sus a ouvert l&rsquo;esprit des disciples pour comprendre ce que disent les &Eacute;critures &agrave; son sujet, (<span class="popup-link" @click = "popUp('pop3')"> Luc 24:44-49</span>).

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">44&nbsp;</sup>Puis il leur dit: C&#39;est l&agrave; ce que je vous disais lorsque j&#39;&eacute;tais encore avec vous, qu&#39;il fallait que s&#39;accompl&icirc;t tout ce qui est &eacute;crit de moi dans la loi de Mo&iuml;se, dans les proph&egrave;tes, et dans les psaumes.</p>

	<p><sup class="versenum">45&nbsp;</sup>Alors il leur ouvrit l&#39;esprit, afin qu&#39;ils comprissent les &Eacute;critures.</p>

	<p><sup class="versenum">46&nbsp;</sup>Et il leur dit: Ainsi il est &eacute;crit que le Christ souffrirait, et qu&#39;il ressusciterait des morts le troisi&egrave;me jour,</p>

	<p><sup class="versenum">47&nbsp;</sup>et que la repentance et le pardon des p&eacute;ch&eacute;s seraient pr&ecirc;ch&eacute;s en son nom &agrave; toutes les nations, &agrave; commencer par J&eacute;rusalem.</p>

	<p><sup class="versenum">48&nbsp;</sup>Vous &ecirc;tes t&eacute;moins de ces choses.</p>

	<p><sup class="versenum">49&nbsp;</sup>Et voici, j&#39;enverrai sur vous ce que mon P&egrave;re a promis; mais vous, restez dans la ville jusqu&#39;&agrave; ce que vous soyez rev&ecirc;tus de la puissance d&#39;en haut.</p>
	<!-- end bible --></div>
	&nbsp;Maintenant, par le Saint-Esprit, Pierre pouvait utiliser les &Eacute;critures pour interpr&eacute;ter les r&eacute;cents &eacute;v&eacute;nements (<span class="popup-link" @click = "popUp('pop4')"> Jo&euml;l 2:28-32</span>,&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">28&nbsp;</sup>Apr&egrave;s cela, je r&eacute;pandrai mon esprit sur toute chair; Vos fils et vos filles proph&eacute;tiseront, Vos vieillards auront des songes, Et vos jeunes gens des visions.</p>

	<p><sup class="versenum">29&nbsp;</sup>M&ecirc;me sur les serviteurs et sur les servantes, Dans ces jours-l&agrave;, je r&eacute;pandrai mon esprit.</p>

	<p><sup class="versenum">30&nbsp;</sup>Je ferai para&icirc;tre des prodiges dans les cieux et sur la terre, Du sang, du feu, et des colonnes de fum&eacute;e;</p>

	<p><sup class="versenum">31&nbsp;</sup>Le soleil se changera en t&eacute;n&egrave;bres, Et la lune en sang, Avant l&#39;arriv&eacute;e du jour de l&#39;&Eacute;ternel, De ce jour grand et terrible.</p>

	<p><sup class="versenum">32&nbsp;</sup>Alors quiconque invoquera le nom de l&#39;&Eacute;ternel sera sauv&eacute;; Le salut sera sur la montagne de Sion et &agrave; J&eacute;rusalem, Comme a dit l&#39;&Eacute;ternel, Et parmi les r&eacute;chapp&eacute;s que l&#39;&Eacute;ternel appellera.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop5')"> Psaumes 16:8-11</span>,&nbsp;

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">8&nbsp;</sup>J&#39;ai constamment l&#39;&Eacute;ternel sous mes yeux; Quand il est &agrave; ma droite, je ne chancelle pas.</p>

	<p><sup class="versenum">9&nbsp;</sup>Aussi mon coeur est dans la joie, mon esprit dans l&#39;all&eacute;gresse, Et mon corps repose en s&eacute;curit&eacute;.</p>

	<p><sup class="versenum">10&nbsp;</sup>Car tu ne livreras pas mon &acirc;me au s&eacute;jour des morts, Tu ne permettras pas que ton bien-aim&eacute; voie la corruption.</p>

	<p><sup class="versenum">11&nbsp;</sup>Tu me feras conna&icirc;tre le sentier de la vie; Il y a d&#39;abondantes joies devant ta face, Des d&eacute;lices &eacute;ternelles &agrave; ta droite.</p>
	<!-- end bible --></div>
	&nbsp;<span class="popup-link" @click = "popUp('pop6')"> Psaumes 110:1</span>).&nbsp;

	<div class="popup invisible" id="pop6"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>De David. Psaume. Parole de l&#39;&Eacute;ternel &agrave; mon Seigneur: Assieds-toi &agrave; ma droite, Jusqu&#39;&agrave; ce que je fasse de tes ennemis ton marchepied.</p>
	<!-- end bible --></div>
	Les p&egrave;lerins Juifs, venus de toutes parts du monde romain, ont entendu le message de l&rsquo;&Eacute;vangile au sujet de la vie, le minist&egrave;re, la mort, la r&eacute;surrection et l&rsquo;offre du salut du p&eacute;ch&eacute;. Pierre exhortait les hommes &agrave; se repentir de leurs mauvais habitudes et comportements, et &agrave; s&rsquo;identifier &agrave; J&eacute;sus en se faisant baptiser en Son nom. Il faisait comprendre aux hommes que le message de l&rsquo;&Eacute;vangile n&rsquo;&eacute;tait pas destin&eacute; &agrave; eux seuls, mais aussi &agrave; leurs amis, leurs familles et &agrave; tout le monde. Le message de l&rsquo;&Eacute;vangile offre deux dons gratuits : le pardon des p&eacute;ch&eacute;s qui r&eacute;tablit notre relation avec Dieu, et le Saint-Esprit qui repr&eacute;sente la pr&eacute;sence de Dieu en l&rsquo;homme. La communaut&eacute; des disciples avait exp&eacute;riment&eacute; une croissance exponentielle &agrave; partir de 120 disciples &agrave; 3000 en un jour. J&eacute;sus nous aide d&eacute;j&agrave; &agrave; assurer le succ&egrave;s de la Grande Commission en sauvant les gens de toutes parts du monde romain.</li>
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

			<td class="social" @click="share('lesson', 'Pierre s\'adresse à la foule: ', '/content/M2/fra/multiply3/multiply304.html')">
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