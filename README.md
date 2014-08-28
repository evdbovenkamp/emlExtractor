#emlExtractor
Распаковщик eml файлов, написан на perl, используется ряд CPAN модулей:

	use MIME::Base64;
	use IO::File;
	use Fcntl qw(:flock);
	use Encode qw(decode encode);
	use Term::ANSIColor;
	use MIME::QuotedPrint::Perl;
	
##USAGE:

запускаем emlExtractor и через пробел eml файлы которые надо распаковать, в итоге получает вывод того что удалось распаковать.

	$ path/to/emlExtractor.pl path/to/email.eml path/to/email.eml path/to/email.eml *N

##INFORMATION

в некоторых случаях, в eml письмах встречаются winmail.dat который содержит вложения, я не стал писать свой велосипед на этот случай, так как с этой задачей прекрасно справляется приложение tnef.
на всякий случай прикладываю его тоже.


##PREMISE

я не нашел ни одного распаковщика EML-файлов, которые корректно бы справлялись со своей задачей, самая большая проблема это binary вложения.

##WARNING!!!

eml формат, это ужасный формат, каждый его создает как хочет, поэтому грамотно и красиво распарсить его очень тяжело, на данный момент emlExtractor содержит тот функционал который решает те задачи которые стояли передо мной, велика вероятность, что вы встретите другой способ формирования eml файла, с которым emlExtractor не справится!
это пре пре пре альфа версия, в ней много слабых мест, г**-кода и т.д. НО думаю при должном желании вы сможете допилить функционал под себя.

Все это поставляется как есть, и не факт что что-то буду доделывать.

