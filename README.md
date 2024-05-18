# 키친포스

## 퀵 스타트

```sh
cd docker
docker compose -p kitchenpos up -d
```

## 요구 사항

### 상품

- 상품을 등록할 수 있다.
- 상품의 가격이 올바르지 않으면 등록할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 이름이 올바르지 않으면 등록할 수 없다.
    - 상품의 이름에는 비속어가 포함될 수 없다.
- 상품의 가격을 변경할 수 있다.
- 상품의 가격이 올바르지 않으면 변경할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 가격이 변경될 때 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 크면 메뉴가 숨겨진다.
- 상품의 목록을 조회할 수 있다.

### 메뉴 그룹

- 메뉴 그룹을 등록할 수 있다.
- 메뉴 그룹의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴 그룹의 이름은 비워 둘 수 없다.
- 메뉴 그룹의 목록을 조회할 수 있다.

### 메뉴

- 1 개 이상의 등록된 상품으로 메뉴를 등록할 수 있다.
- 상품이 없으면 등록할 수 없다.
- 메뉴에 속한 상품의 수량은 0 이상이어야 한다.
- 메뉴의 가격이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴는 특정 메뉴 그룹에 속해야 한다.
- 메뉴의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 이름에는 비속어가 포함될 수 없다.
- 메뉴의 가격을 변경할 수 있다.
- 메뉴의 가격이 올바르지 않으면 변경할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴를 노출할 수 있다.
- 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 높을 경우 메뉴를 노출할 수 없다.
- 메뉴를 숨길 수 있다.
- 메뉴의 목록을 조회할 수 있다.

### 주문 테이블

- 주문 테이블을 등록할 수 있다.
- 주문 테이블의 이름이 올바르지 않으면 등록할 수 없다.
    - 주문 테이블의 이름은 비워 둘 수 없다.
- 빈 테이블을 해지할 수 있다.
- 빈 테이블로 설정할 수 있다.
- 완료되지 않은 주문이 있는 주문 테이블은 빈 테이블로 설정할 수 없다.
- 방문한 손님 수를 변경할 수 있다.
- 방문한 손님 수가 올바르지 않으면 변경할 수 없다.
    - 방문한 손님 수는 0 이상이어야 한다.
- 빈 테이블은 방문한 손님 수를 변경할 수 없다.
- 주문 테이블의 목록을 조회할 수 있다.

### 주문

- 1개 이상의 등록된 메뉴로 배달 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 포장 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 매장 주문을 등록할 수 있다.
- 주문 유형이 올바르지 않으면 등록할 수 없다.
- 메뉴가 없으면 등록할 수 없다.
- 매장 주문은 주문 항목의 수량이 0 미만일 수 있다.
- 매장 주문을 제외한 주문의 경우 주문 항목의 수량은 0 이상이어야 한다.
- 배달 주소가 올바르지 않으면 배달 주문을 등록할 수 없다.
    - 배달 주소는 비워 둘 수 없다.
- 빈 테이블에는 매장 주문을 등록할 수 없다.
- 숨겨진 메뉴는 주문할 수 없다.
- 주문한 메뉴의 가격은 실제 메뉴 가격과 일치해야 한다.
- 주문을 접수한다.
- 접수 대기 중인 주문만 접수할 수 있다.
- 배달 주문을 접수되면 배달 대행사를 호출한다.
- 주문을 서빙한다.
- 접수된 주문만 서빙할 수 있다.
- 주문을 배달한다.
- 배달 주문만 배달할 수 있다.
- 서빙된 주문만 배달할 수 있다.
- 주문을 배달 완료한다.
- 배달 중인 주문만 배달 완료할 수 있다.
- 주문을 완료한다.
- 배달 주문의 경우 배달 완료된 주문만 완료할 수 있다.
- 포장 및 매장 주문의 경우 서빙된 주문만 완료할 수 있다.
- 주문 테이블의 모든 매장 주문이 완료되면 빈 테이블로 설정한다.
- 완료되지 않은 매장 주문이 있는 주문 테이블은 빈 테이블로 설정하지 않는다.
- 주문 목록을 조회할 수 있다.

## 용어 사전
### 공통
| 한글명   | 영문명              | 설명                         |
|-------|------------------|----------------------------|
| 손님    | Guest            | 가게의 메뉴들을 주문할 수 있는 사람을 말한다. |
| 비속어   | Profanity        | 서비스에서 사용하기에 부적절한 단어를 말한다.  |


### 상품
| 한글명   | 영문명              | 설명                    |
|-------|------------------|-----------------------|
| 상품    | Product          | 손님에게 제공할 수 있는 서비스 이다. |

## 메뉴그룹
| 한글명   | 영문명              | 설명                            |
|-------|------------------|-------------------------------|
| 메뉴 그룹 | MenuGroup        | 특정한 목적을 가지고 메뉴들을 묶는 것을 의미한다.  |


### 메뉴
| 한글명   | 영문명              | 설명                               |
|-------|------------------|----------------------------------|
| 메뉴    | Menu             | 손님에게 판매할 수 있는 서비스 정보를 의미한다.   |
| 메뉴 상태 | MenuStatus       | 테이블의 공개가능여부를 상태로 나타낸 것을 의미한다.    |
| 메뉴상품  | MenuProduct      | 메뉴를 구성하기 위해 상품에 순서와 개수를 부여한 것이다. |

### 주문테이블
| 한글명   | 영문명              | 설명                             |
|-------|------------------|--------------------------------|
| 주문 테이블 | OrderTable       | 손님이 매장 주문시 사용할 수 있는 테이블을 의미한다. |
| 테이블 상태 | TableStatus      | 테이블의 사용가능여부를 상태로 나타낸 것을 의미한다.  |
| 방문한 손님 수 | NumberOfGuests   | 특정 주문테이블을 사용중인 손님 수를 의미한다.     |

### 주문
| 한글명   | 영문명           | 설명                                                                               |
|-------|---------------|----------------------------------------------------------------------------------|
| 주문    | Order         | 손님이 제공받길 원하는 메뉴들의 요청을 의미한다.                                                      |
| 주문 항목 | OrderLineItem | 손님이 주문한 메뉴에 대한 정보를 의미한다.                                                         |
| 주문 유형 | OrderType     | 사용자가 주문 항목을 제공받기 위한 방법을 의미한다. 배달, 포장, 매장 식사 유형이 있다.                              |
| 배달    | delivery      | 손님이 배달주소로 음식을 전달해주길 요청하는 유형을 의미한다.                                               |
| 포장    | Takeout       | 손님이 직접 음식을 가지고 가는 유형을 의미한다.                                                      |
| 매장 식사 | EatIn         | 손님이 주문테이블에서 음식을 식사하는 유형을 의미한다.                                                   |
| 주문 상태 | OrderStatus   | 손님이 주문한 메뉴들을 접수에서 완료까지의 상태를 표시한다. 대기중, 준비중, 서빙 완료, 배달 시작, 배달 완료, 주문 완료로 구성되어 있다. |
| 대기중   | Waiting       | 주문이 접수된 상태를 의미한다.                                                                |
| 준비중   | Accepted      | 주문이 수락되어 주문항목들을 준비중인 상태를 의미한다.                                                   |
| 서빙 완료 | Served        | 주문 항목들의 제공이 완료된 상태를 의미한다.                                                        |
| 배달 시작 | Delivering    | 제공된 주문 항목들의 배달이 시작된 상태를 의미한다.                                                    |
| 배달 완료 | Deliverd      | 제공된 주문 항목들의 배달이 완료된 상태를 의미한다.                                                    |
| 주문 완료 | Completed     | 주문이 종료된 상태를 의미한다.                                                                |
| 배달 주소 | DeliveryAddress | 손님이 주문한 메뉴들을 배달하기 위한 주소를 의미한다.                                                   |
| 배달 대행사 | DeliveryAgent | 배달을 선택한 손님들에게 주문한 메뉴들을 전달해주는 역할을 담당한다.                                           |


## 모델링
