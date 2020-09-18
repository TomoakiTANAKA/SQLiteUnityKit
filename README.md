# SQLiteUnityKit �����~���ɂ������C�u����
- ��������SQLiteUnityKit�̉��C�̂ЂƂł��B
- [���|�W�g��](https://github.com/tetr4lab/SQLiteUnityKit) (GitHub)

### ����
- ���{�ꂪ�g����悤�ɂ��܂����B
- �g�����U�N�V���������ɑΉ����܂����B
- �o�C���h�ϐ��ɑΉ����܂����B
- ����DB���㏑�����Ȃ��悤�ɂ��܂����B(���Ƃ����āA�}�[�W�����܂���B)
- �I�[�v����N���[�Y�A���\�[�X�̊J���ȂǂƂ������჌�x�������͉B�����āA���ۉ����x���̍�������������\�ɏo���悤�ɂ��܂����B
- �ł��邾����O�͓����ő����āA���\�[�X�̖����������ē���������悤�ɖ��߂܂����B

# �O��
### ��
- Unity 2019.4.10f1 (LTS)
- Unity 2018.4.26f1 (LTS)
- Unity 2017.4 (LTS)
- SQlite 3.33.0
- C# 6
    - ������⊮(string interpolation)���g�p���Ă��܂��B
    - �K�v�Ȃ�A`PlayerSettings`��`Scripting Runtime Version`��`4.x`�ɐݒ肵�Ă��������B

### SQLite
- SQLite�́ASQL�̃T�u�Z�b�g���g����X�^���h�A���[���ȃf�[�^�x�[�X�Ǘ��V�X�e���ł��B
    - Windows�AMacOS�AAndroid�AiOS�ȂǂɑΉ����Ă��܂��B
- [�����T�C�g](https://www.sqlite.org/index.html)

### SQLiteUnityKit
- SQLiteUnityKit�́AUnity����SQLite���g�p���邽�߂̃t���[�����[�N�ł��B
- [���|�W�g��](https://github.com/Busta117/SQLiteUnityKit) (GitHub)

# �����ƊT�v
- ���|�W�g������`Assets`���v���W�F�N�g�֓������Ă��������B

### �T�v
- `Assets/Plugins/sqlite3/`
    - �e�v���b�g�t�H�[��������SQLite�v���O�C���ł��B(iOS��OS���ŃT�|�[�g������܂��B)
- `Assets/Scripts/`
    - `SQLiteUnity.cs`
        - �K�{�����ł��B
    - "SQLiteUnityUtility.cs"
        - �g�����[�e�B���e�B�N���X�ł��B���D�݂łǂ����B
        - �g�����U�N�V�����ł��[���I�ȃo�C���h���g����悤�ɂȂ��Ă��܂��B
    - "Test.cs"
        - �f���p�X�N���v�g�ł��B
- `Assets/Prefabs/Console.prefab`
    - �f���p�v���n�u�ł��B
- `Assets/Scenes/SQLite_Test.unity`
    - �f���p�V�[���ł��B

### �ŐV�v���O�C���ւ̍X�V
- [�����T�C�g�̃_�E�����[�h](https://www.sqlite.org/download.html)����ŐV�ł�����Ă���`Assets/Plugins`�֓������Ă��������B
- Android�ɂ��ẮA[������̋L��(Qiita)](https://qiita.com/tetr4lab/items/729008c94daaff82833e)���Q�l�ɂ��Ă��������B

# ��{�I�Ȏg����
  - �f�[�^�x�[�X
    - `public class SQLite : IDisposable`
    - �V�K���� (�������N�G��) (���ɂ���ΒP�Ɏg���A��������΃R�s�[���Ďg��)
      - `public SQLite (string dbName, string query = null)`
    - �P�������s
      - `public void ExecuteNonQuery (string query, SQLiteRow param = null)`
    - �P�������s���Č��ʂ�Ԃ�
      - `public SQLiteTable ExecuteQuery (string query, SQLiteRow param = null)`
    - �P���̕ϐ��������ւ��Ȃ��珇�Ɏ��s
      - `public void ExecuteNonQuery (string query, SQLiteTable param)`
      - ����SQL�����A�p�����[�^��ς��Ȃ���J��Ԃ����s���܂��B
    - �������ꊇ���s���A��肪����Ί����߂�
      - `public bool TransactionQueries<T> (T query) where T : IEnumerable<string>`
      - `public bool TransactionQueries (string query)`
      - �����s��z��⃊�X�g�œn�����A�P�ꕶ����Ƃ��ēn�����A�Ƃ����Ⴂ�ł��B
      - �`���Ɩ�����`BEGIN`,`COMMIT`������ɕt���܂��B
  - �s��f�[�^
    - `public class SQLiteTable`
    - �N�G���ŕԂ����f�[�^�ŁA��̒�`�ƍs�f�[�^�̏W���ł��B
  - �s�f�[�^ / �o�C���h�p�����[�^
    - `public class SQLiteRow : Dictionary<string, object>`
    - 1�s���̃f�[�^�ŁA��f�[�^�̏W���ł��B�o�C���h�p�����[�^��n���Ƃ��ɂ��g���܂��B
  - �g���o�C���h (�g�����U�N�V�����p)
    - `public static string SQLiteBind (this string query, SQLiteRow param)`
    - sqlite�̊O���ōs���镶����x�[�X�̃o�C���h�ł��B

# ���̑�
  - ���w�E�₲��āA���邢�͂�����Ȃǂ����}���܂��B
    - �펯�I�Ȃ��Ƃ��������Ă��Ȃ��̂ŁA�����ԈႦ�Ă���悤�ȏꍇ�͂���������������Ə�����܂��B
  - ���ڂ����g�����ɂ��ẮA�g�p����L���ɂ������ƍl���Ă��܂��B
