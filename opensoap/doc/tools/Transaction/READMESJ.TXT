OpenSOAP Transaction Service �h�L�������g
2002/2/28
�g�����U�N�V�����Ǘ��T�[�r�X�{�̂́Csrc/tools/Transaction/�ɂ���܂��D
Client�Ɠ��o���T�[�r�X�̃T���v����samples/Transaction/�ɂ���܂��D

�P�D�T�v
OpenSOAP Transaction Service�i�ȉ��C�g�����U�N�V�����T�[�r�X�j�́C�ȉ�
�̋@�\���������܂��D
�E�d�l�ɂ��������ĕ����̗v�����b�Z�[�W�����ꂼ��SOAP Bodyblock�Ƃ��đ}
  �����ꂽSOAP���b�Z�[�W(SOAP Envelope)���N���C�A���g����󂯎��(��P)
  �ƁC���ꂼ���v�����b�Z�[�W�Ƃ���Envelope�𕪊�����(��Q)���C�w�肳
  �ꂽ�eURL(endpoint)�ɑ��M���܂��D
�E�g�����U�N�V�����T�[�r�X�ɑΉ������e�T�[�r�X����C�d�l�ɂ��������ĕ�
  �����b�Z�[�W���󂯎��ƁC�e�T�[�r�X�̏����̐����E���s�ɉ����āC
  COMMIT�v���C��������ROLLBACK�v�����đ����܂��D
�E�e�T�[�r�X����̃��X�|���X���b�Z�[�W�ƁC�ŏI�I�ȏ������ʁiCOMMIT�܂�
  ��ROLLBACK�j���N���C�A���g�ɕԑ����܂��D
�EOpenSOAP�T�[�o�ƘA�g���邱�ƂŁC�N���C�A���g�͔񓯊��I�ɍŏI���b�Z�[
  �W���󂯎�邱�Ƃ��o���܂��D

�g�����U�N�V�����T�[�r�X�𗘗p���邽�߂ɂ́C�N���C�A���g�ƁC�g�����U�N
�V�����T�[�r�X����ڑ������e�T�[�r�X���g�����U�N�V�����T�[�r�X�ɑΉ�
���Ă���K�v������܂��D


�Q�D�N���C�A���g�d�l�i���N�G�X�g���b�Z�[�W�j
�N���C�A���g�͈ȉ��̎d�l�ɏ]�������N�G�X�g���b�Z�[�W�𑗐M�ł���K�v��
����܂��D

2.1.�g�����U�N�V��������L�q�u���b�N
���N�G�X�g���b�Z�[�W��Body�i<SOAP-ENV:Body>�j�Ɋ܂܂��ŏ���Bodyblock
��<TransactionControl>�ł���K�v������܂�(��P)�D<TransactionControl>
�u���b�N��namespace��"http://services.opensoap.jp/transaction/"�ł���
���Ƃ��]�܂����ł��D
<TransactionControl>�u���b�N�ɂ́C�g�����U�N�V���������̑ΏۂƂȂ�T�[
�r�X�̐������C�q�v�f<endpoint>���C�v������鏈���̏��Ԃɕ���ł���K�v
������܂��D
<endpoint>�v�f�ɂ͊e�T�[�r�X���g�����U�N�V���������Ƃ��Ď��s�\��SOAP
���b�Z�[�W�̑��M��URL���L�q���܂��D�܂��C�e�v���������ƂɌŗL�̔C�ӂ�
�����l"transactionRequestID"��t�����܂��D
���̑��C�g�����U�N�V���������Ɋւ�鏈���ݒ�͂��̃u���b�N�ɋL�q�����
���D�i���łł̎�����<endpoint>�v�f�̂݁j

2.2.�g�����U�N�V�����w�b�_�u���b�N
�e�T�[�r�X�ɑ��M�����ׂ����b�Z�[�W�̃w�b�_�������݂���ꍇ�C�g�����U
�N�V�����w�b�_�u���b�N<TransactionHeaderBlock>�̗v�f�Ƃ��ċL�q���܂�
(��P)�D���̕����ɋL�q���ꂽ�v�f�́C�e�T�[�r�X�ɑ��M�����SOAP���b�Z�[
�W�̃w�b�_�u���b�N�i<SOAP-ENV:Header>�̒����̃u���b�N�j�Ƃ��đ}������
�܂��D<TransactionHeaderBlock>�u���b�N��namespace��
"http://services.opensoap.jp/transaction/"�ł��邱�Ƃ��]�܂����ł��D

�e<TransactionHeaderBlock>�u���b�N�ɂ́C<TransactionControl>�u���b�N��
<endpoint>�v�f�̑Ή����鑮���l"transactionRequestID"��t������K�v����
��܂��D<TransactionHeaderBlock>�u���b�N�͑�QBodyblock�ȍ~�ł���΁C
�ǂ̏��Ԃő}������Ă��Ă����܂��܂���D

2.3.�g�����U�N�V�����{�f�B�u���b�N
�e�T�[�r�X�ɑ��M�����ׂ����b�Z�[�W�̃{�f�B���́C�g�����U�N�V�����{�f�B
�u���b�N<TransactionBodyBlock>�̗v�f�Ƃ��ċL�q���܂�(��P)�D���̕�����
�L�q���ꂽ�v�f�́C�e�T�[�r�X�ɑ��M�����SOAP���b�Z�[�W�̃{�f�B�u���b�N
�i<SOAP-ENV:Body>�̒����̃u���b�N�j�Ƃ��đ}������܂��D
<TransactionBodyBlock>�u���b�N��namespace��
"http://services.opensoap.jp/transaction/"�ł��邱�Ƃ��]�܂����ł��D

�e<TransactionBodyBlock>�u���b�N�ɂ́C<TransactionControl>�u���b�N��
<endpoint>�v�f�̑Ή����鑮���l"transactionRequestID"��t������K�v����
��܂��D<TransactionBodyBlock>�u���b�N���C<TransactionHeaderBlock>�u���b
�N���l�C��QBodyblock�ȍ~�ł���΁C�ǂ̏��Ԃő}������Ă��Ă����܂���
����D


��P. OpenSOAP Transaction Request Envelope
A��s�ɏo���̗v�������C���ꂪ�󂯓����ꂽ��B��s�ɓ��z�̓����v������
��g�����U�N�V�����̗�D

<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/">
<SOAP-ENV:Body>
	<t:TransactionControl xmlns:t="http://services.opensoap.jp/transaction/">
		<endpoint transactionRequestID="1">http://opensoap.jp/cgi-bin/soapInterface.cgi</endpoint>
		<endpoint transactionRequestID="2">http://opensoap.jp/cgi-bin/b_bank_transfer.cgi</endpoint>
	</t:TransactionControl>
	<t:TransactionBodyBlock xmlns:t="http://services.opensoap.jp/transaction/" transactionRequestID="1">
		<p:PaymentRequest xmlns:p="http://services.opensoap.jp/a_bank_transfer/">
			<account>1338675</account>
			<amount>$5000</amount>
			<to>b_bank:1252412</to>
		</p:PaymentRequest>
	</t:TransactionBodyBlock>
	<t:TransactionHeaderBlock transactionRequestID="2" xmlns:tp="http://services.opensoap.jp/transaction/">
		<e:encrypt xmlns:e="http://security.opensoap.jp/1.0/" api="OpenSOAP">true</e:encrypt>
	</t:TransactionHeaderBlock>
	<t:TransactionBodyBlock xmlns:t="http://services.opensoap.jp/transaction/" transactionRequestID="2">
		<d:DepositRequest xmlns:d="http://services.opensoap.jp/b_bank_transfer/">
			<account>1252412</account>
			<amount>$5000</amount>
			<from>a_bank:1338675<from>
		</d:DepositRequest>
	</t:TransactionBodyBlock>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>


�R�D�g�����U�N�V�����Ή��T�[�r�X�d�l
OpenSOAP Transaction Service�ɑΉ������T�[�r�X�́C�N���C�A���g��������
��SOAP���b�Z�[�W�̎d�l�i�w�b�_�u���b�N�C�{�f�B�u���b�N�̓��e�j�ƃT�[�r
�X�̋@�\���N���C�A���g�Ɍ��J����Ƌ��ɁC�g�����U�N�V�����T�[�r�X�Ƃ̐�
���ɂ��āC�ȉ��̎d�l�ɏ]���K�v������܂��D

3.1.�v�������ɑ΂���ԐM
�g�����U�N�V�����T�[�r�X�ɂ���ĕ����������ꂽ�eEnvelope(��Q)�́C�Ή�
���邻�ꂼ���endpoint�ɑ��M����܂��D�e�T�[�r�X�́CEnvelope�ɂ�������
�ėv�����ꂽ�������s���C���̏�����Rollback�ł����Ԃŕۑ�������C���X
�|���X���b�Z�[�W(��R)���g�����U�N�V�����T�[�r�X�ɕԐM���܂��D���X�|��
�X���b�Z�[�W�̎d�l�͊e�T�[�r�X���ƓƎ��ł��܂��܂��񂪁C��1�{�f�B�u���b
�N�̒����ɂ͏����̌��ʂ��L�q����q�v�f<TransactionResult>���܂ޕK�v��
����܂��D
<TransactionResult>�ɂ́C���̃T�[�r�X�ł̏����̐�����ʒm����"SUCCESS"
���L�q���܂��D����ȊO�̕�����C�������̓T�[�r�X����<SOAP-ENV:Fault>��
���ԐM���ꂽ�ꍇ�́C���̃T�[�r�X�ł̏����͎��s�C�������͋��ۂ��ꂽ����
�Ƃ݂Ȃ���܂��D
�܂��C<TransactionResult>�ɂ́C�T�[�r�X���ŌŗL�̎���ID�𑮐��l
"transactionID"�Ƃ��ĕt�����邱�Ƃ��ł��܂��D"transactionID"�������g��
�ƁC���̃X�e�b�v�Ńg�����U�N�V�����T�[�r�X����COMMIT�܂���ROLLBACK�̗v
�����Ȃ��ꂽ���ɁC�T�[�r�X���Ő������Ƃ邱�Ƃ��ł��܂��D

3.2.COMMIT�܂���ROLLBACK�v��
�g�����U�N�V�����T�[�r�X�̓T�[�r�X���琬���i"SUCCESS"�j���ԐM�����ƁC
<TransactionControl>�u���b�N�ɋL�q���ꂽ���Ԃɏ]���Ď��̃T�[�r�X�ւ̃�
�N�G�X�g���b�Z�[�W�𑗐M���܂��D
�S�ẴT�[�r�X����SUCCESS���ԐM���ꂽ�ꍇ�C�g�����U�N�V�����T�[�r�X��
�ĂёS�Ă�endpoint�ɑ΂��đΉ�����"transactionID"�����l��t������
COMMIT�v�����b�Z�[�W(��S)�𑗐M���Ĉ�A�̏����̎��s�����肵�܂��D
�S�ẴT�[�r�X����SUCCESS���ԐM�����O�ɁC�r���̃T�[�r�X���玸�s���b
�Z�[�W���ԐM�����ƁC���̑O�܂ł�SUCCESS���ԐM���ꂽ�T�[�r�X�Q�ɑ΂�
��"transactionID"�����l��t������ROLLBACK�v�����b�Z�[�W�𑗐M���܂��D

3.3.�����̊���
COMMIT�v�����󂯎�����T�[�r�X�͗v�����ꂽ���������s���ďI�����C
ROLLBACK�v�����󂯎�����T�[�r�X�͑Ή����鏈�����������܂��D����ɁC
�g�����U�N�V�����T�[�r�X�ɂ��ꂼ��̏��������������|��SOAP���b�Z�[�W
(��T)��ԐM���܂��D


��Q(A)�DA��s�֑��M�����SOAP Envelope

<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
<SOAP-ENV:Body>
<p:PaymentRequest xmlns:p="http://services.opensoap.jp/a_bank_transfer/">
	<account>1338675</account>
	<amount>$5000</amount>
	<to>b_bank:1252412</to>
</p:PaymentRequest>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>

��Q(B)�DB��s�֑��M�����SOAP Envelope

<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
<SOAP-ENV:Body>
<d:DepositRequest xmlns:d="http://services.opensoap.jp/b_bank_transfer/">
	<account>1252412</account>
	<amount>$5000</amount>
	<from>a_bank:1338675</from>
</d:DepositRequest>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>

��R�DA��s����̃��X�|���X�̗�

<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
<SOAP-ENV:Body>
<p:PaymentResponse xmlns:p="http://services.opensoap.jp/samples/a_bank_transfer/">
	<t:TransactionResult xmlns:t="http://services.opensoap.jp/transaction/" transactionID="abank13386751012192663">
	SUCCESS
	</t:TransactionResult>
	<p:Comment>1338675 sent $5000 to b_bank:1252412</p:Comment>
</p:PaymentResponse>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>


��S�D�g�����U�N�V�����T�[�r�X����A��s�ւ�COMMIT�v��

<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
<SOAP-ENV:Body>
	<t:TransactionAction xmlns:t="http://services.opensoap.jp/transaction/" transactionID="abank13386751012192663">
	COMMIT
	</t:TransactionAction>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>


��T�DA��s����COMMIT�v���ɑ΂���ԐM

<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
<SOAP-ENV:Body>
	<t:TransactionActionResponse xmlns:t="http://services.opensoap.jp/transaction/" transactionID="abank13386751012192663">
	COMMITED
	</t:TransactionActionResponse>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>

�S�D�N���C�A���g�ւ̕ԐM
�g�����U�N�V�����T�[�r�X�́C��A�̏����̌��ʂ����N�G�X�g���b�Z�[�W�Ɠ�
�l�ɂЂƂ�Envelope�Ɍ�����(��U�j�C�N���C�A���g�ɕԐM���܂��DSOAP���b
�Z�[�W�̍ŏ��̃{�f�B�u���b�N<TransactionResponse>�u���b�N�ɂ́C�g����
�U�N�V�����̍ŏI���ʂ��CCOMMIT�܂���ROLLBACK�Ƃ��ċL�q����܂��D�Q��
�ȍ~�̃{�f�B�u���b�N�́C�e�T�[�r�X����ԐM���ꂽ���X�|���X���b�Z�[�W��
�w�b�_�u���b�N��<TransactionHeaderBlock>�u���b�N�ɁC�{�f�B�u���b�N��
<TransactionBodyBlock>�u���b�N�ɁC�����COMMIT��������ROLLBACK�𑗐M��
���ۂ̃��X�|���X���b�Z�[�W�̃{�f�B�u���b�N��
<TransactionActionResponseBodyBlock>�ɁC���ꂼ�ꃊ�N�G�X�g���b�Z�[�W��
�t�����������l"transactionRequestID"�Ɠ��������l���t������đ}�������
���D


��U�D�N���C�A���g�ɕԐM�����g�����U�N�V������������

<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
<SOAP-ENV:Body>
	<t:TransactionResponse xmlns:t="http://services.opensoap.jp/transaction/">
	COMMIT
	</t:TransactionResponse>
	<t:TransactionBodyBlock xmlns:t="http://services.opensoap.jp/transaction/" transactionRequestID="1">
		<p:PaymentResponse xmlns:p="http://services.opensoap.jp/samples/a_bank_transfer/">
			<t:TransactionResult transactionID="pt13386751012192663">
				SUCCESS
			</t:TransactionResult>
			<:Comment xmlns:="">
				1338675 sent $5000 to b_bank:1252412
			</:Comment>
		</p:PaymentResponse>
	</t:TransactionBodyBlock>
	<t:TransactionActionResponseBodyBlock xmlns:t="http://services.opensoap.jp/transaction/" transactionRequestID="1">
		<t:TransactionActionResponse transactionID="pt13386751012192663">
			COMMITED
		</t:TransactionActionResponse>
	</t:TransactionActionResponseBodyBlock>
	<t:TransactionBodyBlock xmlns:t="http://services.opensoap.jp/transaction/" transactionRequestID="2">
		<p:DepositResponse xmlns:p="http://services.opensoap.jp/samples/a_bank_transfer/">
			<t:TransactionResult transactionID="dt12524121012226863">
				SUCCESS
			</t:TransactionResult>
			<p:Comment>
				1252412 received $5000 from a_bank:1338675
			</p:Comment>
		</p:DepositResponse>
	</t:TransactionBodyBlock>
	<t:TransactionActionResponseBodyBlock xmlns:t="http://services.opensoap.jp/transaction/" transactionRequestID="2">
		<t:TransactionActionResponse transactionID="dt12524121012226863">
			COMMITED
		</t:TransactionActionResponse>
	</t:TransactionActionResponseBodyBlock>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>