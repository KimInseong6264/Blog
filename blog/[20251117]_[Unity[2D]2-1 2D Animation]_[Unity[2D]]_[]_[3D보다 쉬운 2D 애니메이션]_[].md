애니메이션




![](https://velog.velcdn.com/images/iissk/post/992acf57-f59d-4623-b9ec-22bc6da8569c/image.png)


2D 애니메이션 기능 코드 만들기
```
public Sprite[] frames;
public float frameRate = 0.1f;

// 스프라이트 랜더러에 여러 스프라이트를 넣고 재생 시킬 것임
private SpriteRenderer spriteRenderer;

private int currentFrame = 0;
private Coroutine animationCoroutine;
private WaitForSeconds delay;


private void Awake()
{
    spriteRenderer = GetComponent<SpriteRenderer>();
    if (spriteRenderer == null)
    {
        Debug.LogError("SpriteRender가 없음");
    }

    delay = new WaitForSeconds(frameRate);
}

private void OnEnable()
{
    StartAnimation();
}

private void OnDisable()
{
    StopAnimation();
}

private void StartAnimation()
{
    if (animationCoroutine != null)
    {
        StopCoroutine(animationCoroutine);
    }

    animationCoroutine = StartCoroutine(PlayAnimation());
}

private void StopAnimation()
{
    if (animationCoroutine != null)
    {
        StopCoroutine (animationCoroutine);
    }
}

// frameRate에 맞춰서 이미지를 바꾸는 애니메이션
private IEnumerator PlayAnimation()
{
    while (true)
    {
        if (frames.Length > 0)
        {
            spriteRenderer.sprite = frames[currentFrame];
            currentFrame = (currentFrame + 1) % frames.Length;
        }
        yield return delay;
    }
}
```