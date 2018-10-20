# alps-touchpad-kext_and_prefpane_to-high-sierra
Kext VoodooPs2 modificada para touchpad alps e painel de preferências 
Testada no notebook Dell Vostro 3460

![Preferencias](https://github.com/marcosandrade22/alps-touchpad-kext_and_prefpane_to-high-sierra/blob/master/Captura%20de%20Tela%202018-10-20%20a%CC%80s%2015.08.09.png?raw=true)
<p>
Para instalação pode utilizar o kext utility e instalar em System/Library/Extensions
</p>

<p>
Após a instalação pode ser que o touchpad não seja reconhecido em Preferências do Sistema,
neste caso é necessário a substituição do arquivo Trackpad.prefPane em System/Library/PreferencePanes
</p>
<p>
 Download da prefpane:<br>
 https://drive.google.com/file/d/1FrSYc6zOU0S6jbDEQqFGxzWqfRCyzCOu/view?usp=sharing
 </p>

<p>
Para realizar esta substituição você precisa iniciar por um pendrive de boot pois não terá permissões de escrita no dirtório.
</p>
<p>
Passos recomendados:
</p>

<b>PELO FINDER, AINDA NO SISTEMA INSTALADO</b>
<ul>
  <li>
  1- Faça backup do arquivo Trackpad.prefPane original localizado em System/Library/PreferencePanes
  </li>
  <li>
  2- Copiar o novo arquivo, já extraido, para a raiz do disco.
  </li>
  </ul>
  
<b>PELO PENBOOT</b>
<ul>
  <li>
  3- Iniciar por um penboot e no menu "Utilitários" acessar o terminal.
  </li>
  <li>
  4- remover o arquivo Trackpad.prefPane (lembre do backup no passo 1)
  </li>
  
  > rm -rf System/Library/PreferencePanes/Trackpad.prefPane
  <li>
  5- Copie o novo arquivo para o diretório
  </li>
  
   > cp -R Trackpad.prefPane System/Library/PreferencePanes/
   </ul>
    <p>
 Você pode obter uma mensagem de que "este arquivo é um diretório" para corrigir isso tenha atenção nas barras, 
 cp -R Trackpad.prefPane é diferente de cp -R Trackpad.prefPane/
 </p>
 
 <p>
 <b>Sensibilidade</b>
 Você pode ajustar a sensibilidade do touch pad alterando o parâmetro fingerZ da seguinte forma:
 No arquivo da kext clique com o botão direito e escolha <b>Mostrar conteúdo do pacote</b>, depois vá em <b>Contents/Plugins</b> e na kext VoodooPS2Trackpad clique novamente com o botão direito e <b>Mostrar conteúdo do pacote</b> em Contents edite o arquivo Info.plist e realize o ajuste se necessário, os valores indicados são de 1 a 30.
 </p>
 
 fonte: https://osxlatitude.com/forums/topic/8285-refined-alps-touchpad-driver/?do=findComment&comment=67735
