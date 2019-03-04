# SQLiteUnityKit �����~���ɂ������C�u����
___

## �ύX�_
  * ���{�ꂪ�g����悤�ɂ��܂����B
  * �g�����U�N�V���������ɑΉ����܂����B
  * �o�C���h�ϐ��ɑΉ����܂����B
  * �I�[�v����N���[�Y�A���\�[�X�̊J���ȂǂƂ������჌�x�������͉B�����āA���ۉ����x���̍�������������\�ɏo���悤�ɂ��܂����B
  * �ł��邾����O�͓����ő����āA���\�[�X�̖����������ē���������悤�ɖ��߂܂����B

## �K�v�Ȋ�
  * �e�X�g�́AUnity2017.4��2018.2��Windows��Android�݂̂ōs���܂����B
  * C# 6 �̕�����⊮(string interpolation)���g�p���Ă��܂��B
    * PlayerSettings��Scripting Runtime Version��4.x�ɐݒ肵�Ă��������B

## �����̎d��
  * �ŐV�v���O�C���̓���
    * �����T�C�g����ŐV�ł�����Ă��܂��B
    * �p�b�P�[�W���̃v���O�C�����ɍ��킹��DllImport�̈��������������邩�A�t��AAR�p�b�P�[�W���̃v���O�C������ύX���܂��B
      * �Ȃ��A�p�b�P�[�W������o���Ē��u���ɂ���ƁA�r���h�̍ۂ�Unity�̓����`�F�b�N�Ɉ���������܂��B
  * "SQLiteUnity.cs"
    * �K�{�����ł��B
  * "SQLiteUnityUtility.cs"
    * �g�����[�e�B���e�B�N���X�ł��B���D�݂łǂ����B
    * �g�����U�N�V�����ł��[���I�ȃo�C���h���g����悤�ɂȂ��Ă��܂��B
  * "Test.cs"
     * �K�v����܂���B

## ��{�I�Ȏg����
  * �f�[�^�x�[�X
    * public class SQLite : IDisposable
    * �V�K���� (�������N�G��) (���ɂ���ΒP�Ɏg���A��������΃R�s�[���Ďg��)
      * public SQLite (string dbName, string query = null)
    * �P�������s
      * public void ExecuteNonQuery (string query, SQLiteRow param = null)
    * �P�������s���Č��ʂ�Ԃ�
      * public SQLiteTable ExecuteQuery (string query, SQLiteRow param = null)
    * �P���̕ϐ��������ւ��Ȃ��珇�Ɏ��s
      * public void ExecuteNonQuery (string query, SQLiteTable param)
      * ����SQL�����A�p�����[�^��ς��Ȃ���J��Ԃ����s���܂��B
    * �������ꊇ���s���A��肪����Ί����߂�
      * public bool TransactionQueries<T> (T query) where T : IEnumerable<string>
      * public bool TransactionQueries (string query)
      * �����s��z��⃊�X�g�œn�����A�P�ꕶ����Ƃ��ēn�����A�Ƃ����Ⴂ�ł��B
      * �`���Ɩ�����'BEGIN','COMMIT'������ɕt���܂��B
  * �s��f�[�^
    * public class SQLiteTable
    * �N�G���ŕԂ����f�[�^�ŁA��̒�`�ƍs�f�[�^�̏W���ł��B
  * �s�f�[�^ / �o�C���h�p�����[�^
    * public class SQLiteRow : Dictionary<string, object>
    * 1�s���̃f�[�^�ŁA��f�[�^�̏W���ł��B�o�C���h�p�����[�^��n���Ƃ��ɂ��g���܂��B
  * �g���o�C���h (�g�����U�N�V�����p)
    * public static string SQLiteBind (this string query, SQLiteRow param)
    * sqlite�̊O���ōs���镶����x�[�X�̃o�C���h�ł��B

## ���̑�
  * ���w�E�₲��Ă����}���܂��B
    * �펯�I�Ȃ��Ƃ��������Ă��Ȃ��̂ŁA�����ԈႦ�Ă���悤�ȏꍇ�͂���������������Ə�����܂��B
    * �p���͏����Ȃ��̂ŁA�p��ł������������b�Z�[�W�ɂ����{��ł��Ԃ����܂��B�������e�͂��������B
  * ���ڂ����g�����ɂ��ẮA�ʓr���������������ƍl���Ă��܂��B
