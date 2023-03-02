clear
resp=1
while [ $resp -ne 3]; do
resp=$(dialog --stdout --title ‘O que fazer?’ --menu ‘O que você deseja fazer?’ 0 0 0 1 ‘Ver todos os contatos cadastrados’ 2 ‘Cadastrar um novo contato’ 3 ‘Fechar o programa’ )
if test $resp = 1
then
 (dialog --title ‘Contatos cadastrados’ --textbox /home/vitor/Desktop/Contatos 0 0 )
 clear
else
if test $resp = 3
then
 clear
else
  if test $resp = 2
  then
  fone=$(dialog --stdout --inputbox ‘Digite o telefone:’ 0 0 )
  if  [ $? -eq 1 ];
  then
  echo OK
  else [ $? -eq 0]
  nome=$(dialog --stdout --inputbox ‘Digite o nome:’ 0 0 )
  if  [ $? -eq 1 ];
  then
  echo OK
  else [ $? -eq 0]
  data=$(dialog --stdout --inputbox ‘Digite a data de nascimento:’ 0 0 )
  if  [ $? -eq 1 ];
  then
  echo OK
  else [ $? -eq 0]
  liga=$(dialog --stdout --radiolist ‘Qual a ligação com o contato?’ 0 0 0 Amigo ‘’ on Parente ‘’ off Cliente ‘’ off )
  if  [ $? -eq 1 ];
  then
  echo OK
  else [ $? -eq 0]
  atual=$(date+”%e-%T”)
  (dialog --stdout --msgbox $(date +”%e-%T”) 0 0 )     
  if  [ $? -eq 1 ];
  then
  echo OK
  else [ $? -eq 0]
  dialog --stdout \
    --title ‘Tem certeza?’ \
    --yesno ‘\nDeseja realmente salvar o novo contato?.\n\n’ \
  0 0
  if [ $? == 0];
  then
  sleep 1
  echo $fone >> Contatos;
  echo $nome >> Contatos;
  echo $data >> Contatos;
  echo $liga >> Contatos;
  echo $atual >> Contatos;
  echo ‘--------------------------------------------------------' >>Contatos;
  (dialog --stdout --msgbox “O endereço foi adicionado aos contatos” 0 0 )
  else
  (dialog --stdout --msgbox “Cancelando...” 0 0 )
  sleep 1
fi
fi
fi
fi
fi
fi
fi
fi
fi
done  
